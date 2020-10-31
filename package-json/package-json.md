# Package.json

`package.json` is a json config file that shows details of the package and its dependencies.

the default fields are:

- name – the name of the package
- version – the current version number of the package
- description – a package description, this is used for meta analysis in package registries
- main – the entry-point file to load when the package is loaded
- scripts – namespaced shell scripts, these will be discussed later in this section
- keywords – array of keywords, improves discoverability of a published package
- author – the package author
- license – the package license.

## scripts

the scripts field is used to define aliases for shell commands

### example

``` node
 "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "lint": "standard"
  },
```

### run a script

to call a script use:

`npm run lint`

#### parameters

if you need to pass parameters to scripts you will need `--`

`npm run lint -- --fix`

### script special commands

There are several special commands names that do not need the run command to be called ie `npm test` instead of `npm run test` the full list can be found via: `npm help npm-scripts`

#### popular special script commands

- publish
- test
- install
