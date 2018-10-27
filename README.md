### Ru
---
https://github.com/tombenner/ru

```
ru 'map(:center, 80)' myfile
awk 'printf "%" int(40+length($0)/2) "s\n", $0' myfile
ru 'map(:to_i).sum' myfile
awk '(s+=$1) END {print s}' myfile

ru 'map(:to_i, 10).sum' myfile
ru 'map(:to_i).reduce(&:+)' myfile
ru 'each_line.to_i.to_a.sum' myfile
ru 'grep(/^\d+$/).map(:to_i).sum' myfile
ru 'map { |n| n.to_i }' myfile
ru 'reduce(0) { |n| sum + n.to_i }' myfile
ru 'each_line.match(/(\d+)/)[1].to_i.to_a.sum' myfile
ru 'map { |n| n.to_i }.reduce(0) { |sum, n| sum + n }' myfile

gem install ru

printf "2\n3" | ru 'map(:to_i).sum'

printf "2\n3" | ru 'map(:to_i).sum'
cat myfile | ru 'map(:to_i).sum'

ru 'map(:to_i)' myfile
ru 'map(:to_i).sum' myfile myfile

ru '! 2 + 3'

ru 'map(:center, 80)' myfile
awk 'printf "%" int(40+length($0)/2) "s\n", $0' myfile

ru 'map(:to_i).sum' myfile
awk '{s+=$1} END {print s}' myfile

paste -s -d+ myfile | bc

ru '[4]' myfile
sed '5q;d' myfile

ru '[1..-2]' myfile
sed '1d;$d' myfile

ru 'map { |line| [line[/(\d+)(".+"){2}$/, 1].to_i, line] }.sort.reverse.map(:join, " ")' access.log
awk --re-interval '{match($0, /(([^[:space:]]+|\[^\]]+\]|"[^"]+")[[:space:]]+){7})/, m); print m[2], $0 }'

ru 'each_line.strip.center(80)' myfile
ru 'each_line.strip.to_a.map(:center, 80)' myfile

printf "foo.txt" | ru 'files.map(:updateed_at).map(:strftime, ""%Y-%m-%d")'
ru 'files.format'

printf "john\npaul\ngeorge" | ru 'grep(/o[h|r]/)'

printf "john\npul" | ru 'map(:[], 0)'
printf "john\npual" | ru 'map(:center, 8, ".")'

printf "john\npaul" | ru 'each_line[0]'
printf "john\npaul" | ru 'each_line.center(8, ".")'

ru save sum 'map(:to_i).sum'

printf "2\n3" | ru run sum

ru list

appraisal rspec

```


```
```

```
```
