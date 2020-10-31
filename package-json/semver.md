# semver

all dependencies in node use `semver` version standards.

`2.3.54`

- major
- minor
- patch

## npm installation

When installing packages via npm you can define what version of the package to install
  
To test / confirm ranges use the npm semver calculator: `https://semver.npmjs.com/`

### Fixed version

Install a fixed version and always install it, independant of future releases

`"standard": "14.3.3"`

- this will always install `14.3.3`

### Fixed Major Version (^)

Carets tell npm that you can install future versions of the software within boundaries of `semver minor` releases

`"standard": "^14.3.3"`

- this will allow any minor or patches to standard on major version 14.
- this is the default used for doing a `npm install`

#### Good releases for ^

- 14.3.4
- 14.4.1

#### Bad releases for ^

- 15.0.1
- 14.2.1

### Fixed Major and Minor Version (~)

Tilde tell npm that you can install future versions of the software within boundaries of `semver patches` releases

`"standard": "~14.3.3"`

- this will allow any patche to `14.3`
- this is the default used for doing a `npm install`

#### Good releases for ~

- 14.3.4
- 14.3.5

#### Bad releases for ~

- 14.4.1
- 14.3.2
- 15.0.1

## X notation

You can also use x notation. This will allows even greater variance of installs

### 14.x

This will install any version from 14.0.1 to the latest minor

### 14.1.x

This will install any patched version of 14.1. to the latest patch
