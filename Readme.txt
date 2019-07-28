

1. Use the script below to count word statistics

tr '[A-Z]' '[a-z]' < test.txt | tr -cd '[A-Za-z0-9_ \012]' | tr -s '[ ]' '\012' | sort | uniq -c | sort -nr | sed "s/\(^[0-9]*\)\([ ]*\)\([a-z,0-9]*\)/\3: \1/g" | head -n 100 | cat > output.txt


e.g.

replace `test.txt` with your input file nameo

word stats would be write to `output.txt`



2. Then use word cloud website that support generate word cloud with word statistics

e.g. https://worditout.com/word-cloud/create

- use the table option


I test it with 50MB text file, it will take 10 min to 30 mins for 200MB I guess
