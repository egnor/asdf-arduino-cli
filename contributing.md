# Contributing

Testing Locally:

```shell
asdf plugin test <plugin-name> <plugin-url> [--asdf-tool-version <version>] [--asdf-plugin-gitref <git-ref>] [test-command*]

asdf plugin test arduino-cli https://github.com/egnor/asdf-arduino-cli.git "arduino-cli version"
```

Tests are automatically run in GitHub Actions on push and PR.
