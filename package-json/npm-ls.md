# npm ls

returns package dependencies as well as there dependencies.

## example

``` node
`-- pino@6.7.0
  +-- fast-redact@3.0.0
  +-- fast-safe-stringify@2.0.7
  +-- flatstr@1.0.12
  +-- pino-std-serializers@2.5.0
  +-- quick-format-unescaped@4.0.1
  `-- sonic-boom@1.3.0
    +-- atomic-sleep@1.0.0
    `-- flatstr@1.0.12 deduped
```

- `--`    - is a direct dependency of package.json
- `  +--` - is a dependency of the pino
- node `flatstr` is duplicated as its used for `pino` and `sonic-boom`
