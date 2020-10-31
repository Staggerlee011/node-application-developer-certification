# npm outdated

returns all modules in the package.json file that can be updated

`npm outdated`

returns:

``` node
Package   Current  Wanted  Latest  Location  
standard   14.3.4  14.3.4  16.0.1  my-package
```

- `current`: returns the version you currently have installed and in `package-lock.json`
- `wanted`: is the version you will update to via `npm update` based on the `semver` detailed in `package.json`
- `latest`: is the latest version of the package
- `location`: is the name of the package used
