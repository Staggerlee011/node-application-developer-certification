# npm install

installs dependencies

## npm install

if you call npm install on package.json that doesnt have a node_modules folder. It will install all dependencies listed in the file as well as sub dependencies needed

## npm install <pkg>

if you run npm install <package> it will add the dependency to the package.json file and download it to the node_modules folder

``` node
npm install pino
```

``` node
{
  "name": "my-package",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "pino": "^6.7.0"
  }
}
```

## node_modules

after running `npm install` it will create a mode_modules folder which contains the dependencies (As well as any dependcies of that it may have as well)

## development dependencies

sometimes you need to run extra dependencies in a dev environment

`npm install --save-dev standard`

- note this creates `devDependencies` field

``` node
{
  "name": "my-package",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "pino": "^6.2.1"
  },
  "devDependencies": {
    "standard": "^14.3.3"
  }
}
```

### installing only production dependencies

If you run run `npm install` when you have devDependencies it will download all modules including them. For a production install you will need to run `npm install --production`
