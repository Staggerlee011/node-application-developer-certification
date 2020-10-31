# npm install command

- installs dependencies
- npm installs can be either global or local
- if you call npm install on `package.json` that doesnt have a `node_modules` folder. It will install all dependencies listed in the file as well as sub dependencies needed

## global installs -g

to install a global npm package you need to use: `npm install create-reach-app -g`

Once you install a package via the global tag. you can call it from any location. Not restricted to the folder of the `package.json` file

## npm install

- running `npm install` when you have `package.json` file will install all dependencies and sub dependnecies of the file and download them to the `node_modules` folder

## npm install <pkg>

- running `npm install <package>` will add the dependency to `package.json` file and download it to the `node_modules` folder
- if you do not have a `package.json` file it will still create `package-lock.json` and add the file to the `node_modules` folder

``` node
npm install pino
```

``` node
  "dependencies": {
    "pino": "^6.7.0"
  }
```

## development dependencies

- sometimes you need to run extra dependencies in a dev environment (test frameworks, linters etc)
- note this creates `devDependencies` field

`npm install --save-dev standard`
`npm i -D standard`

``` node
  "dependencies": {
    "pino": "^6.2.1"
  },
  "devDependencies": {
    "standard": "^14.3.3"
  }
```

## installing only production dependencies

- For a production install you will need to run `npm install --production`
- If you run run `npm install` when you have devDependencies it will download all modules including them

## define version installed

- `npm install lodash@4.12` installs a specific version
- `npm install lodash@latest` installs the latest version
- `npm install lodash` installs the latest version
