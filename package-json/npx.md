# npx

npx is used to execute packages that are stored the node_modules folder. This is how the `"scripts"` section of package.json works. npx can also be called directly via `npx <package name>`

## examples

having a package.json script with

``` node
"scripts": {
    "test": "jest"
}
```

- if you run `jest` this will fail unless jest is installed globally 
- if you run `npm test` this will work as node will call npx in the background
- if you run `npx jest` this will work
