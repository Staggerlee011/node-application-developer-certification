# Diagnostics 6%

## Debugging Node.js

in order to debug node must be started in `inspect` mode. This runs node in a debug mode. allowing you to run tools like chrome devtools against it

### Start node in insecpt mode

to run node in inspoect mode you use the `--inspect` flag

``` node
node --inspect app.js
```

normally you will want to start with an active breakpoint as the code initializes, this makes it not go into full async mode

``` node
node --inspect-brk app.js

Debugger listening on ws://127.0.0.1:9229/b147043b-8502-4973-ae19-696bbe187d8e
For help, see: https://nodejs.org/en/docs/inspector
```

### Connect to process to debug

- Open chrome: `chrome://inspect`
- Under the title `Remote Target` you will a target now to the file you called in the --insect with a URL (click the link to get a pop up window)

![example chrome://inspect view](img\chrome-inspect-01.JPG)

- note if you ran `--inspect-brk` it will started in `debugger paised`

![example chrome://inspect view](img\chrome-inspect-02.JPG)

### Breakpoints

You can add breakpoints either directly in the code or via devtools:

#### Code breakpoint

`When not debugging, these debugger statements are ignored, however due to noise and potential performance impact it is not good practice to leave debugger statements in code.`

To add a breakpoint in the code add the debugger function  

- see line `3`

``` node
1: function f(n =99){
2:    if (n===0) throw Error()
3:    debugger
4:    f(n-1)
5: }
6: f()
```

#### Chrome devTools

you can add breakpoints by clicking on the line number you want to add the line break in

![example chrome://inspect view](img\chrome-inspect-03.JPG)

## Basic performance analysis
