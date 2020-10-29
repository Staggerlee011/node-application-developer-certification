# npm init

Creates a `package.json` file in the folder the command is run from. It gives you a list of options:

``` node
- package name (Note it will not allow you to use capitals)
  - example: `my-package`
- version (semver default output 1.0.0)
  - example: `1.0.0`
- description 
  - example: `my npm package`
- entry point (default is index.js)
  - example: `index.js`
- test command ()
  - example: ``
- git repository ()
  - example: `https://github.com/Staggerlee011/node-application-developer-certification`
- keywords (Used to search for npm packages)
  - example: `learning, development`
- license: (ISC)
  - example: ``
```

- If you run the command against folder with package.json in it, it will update the file with input changes
- If you run `npm init -y` it will create a `package.json` file with all defaults
- If you run `npm init -y` in the root of a git repo it populate the git repoistory with your URL
