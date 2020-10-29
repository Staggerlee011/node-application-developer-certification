# Node.js CLI 4%

## Node executable command line flags

- Note you have to call the flag before the script for node to load

### node version (-v --version)

returns the version of node installed

``` node
node -v
node --version
```

### check syntax (-c --check)

returns if the javascript parses correctly. If it is correct you get no responce. If it errors you get an output of the error

``` node
node --check
node -c
```

### stack trace output (--stack-trace-limit)

stack traces are generated from errors in code. The number of rows returned for the stack trace can be set via

- Note you have to call the flag before the script for node to load

``` node
node --stack-trace-limit=20 app.js
```

### dynamic evaluation (-e -p)

you can evaluate code from the shell using either `--eval/-e` or `--print/-p`

- print evaluates an expression and prints the result
- eval doesnt return the responce

``` node
PS E:\> node -p "1+1"
2
PS E:\> node -e "1+1"
PS E:\> node --eval "console.log(1+1)"
2
PS E:\> node --print "console.log(1+1)"
2
undefined
```

### preload modules (-r --require)

tells node to preload modules before anything else loads

``` node
PS E:\> node -r ./preload.js app.js
preload.js : this is preloaded
app.js: this is the main file
```

## node_modules

you can delete all the node_modules folder via the below node cli call

- note this command is platform independent

``` node
node -e "fs.rmdirSync('node_modules', {recursive: true})"
```
