# cut command syntax
```
wc -l $1 | cut -d ' ' -f 1
```
# execute commands inside of a shell script
```
$(wc -l $1 | cut -d ' ' -f 1)
```
# call a function from another
```
#!/usr/bin/env bash
foo() {
    echo $result
}
#TODO: get type of each column
bar(){
    result=$(foo $1)
    echo $result
}
bar $1
```