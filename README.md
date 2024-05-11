<div align="center">

# asdf-arduino-cli [![Build](https://github.com/egnor/asdf-arduino-cli/actions/workflows/build.yml/badge.svg)](https://github.com/egnor/asdf-arduino-cli/actions/workflows/build.yml) [![Lint](https://github.com/egnor/asdf-arduino-cli/actions/workflows/lint.yml/badge.svg)](https://github.com/egnor/asdf-arduino-cli/actions/workflows/lint.yml)

[arduino-cli](https://github.com/arduino/arduino-cli) plugin for the [asdf version manager](https://asdf-vm.com).

</div>

# Contents

- [Dependencies](#dependencies)
- [Install](#install)
- [Contributing](#contributing)
- [License](#license)

# Dependencies

- `bash`, `curl`, `tar`, and [POSIX utilities](https://pubs.opengroup.org/onlinepubs/9699919799/idx/utilities.html).
- `SOME_ENV_VAR`: set this environment variable in your shell config to load the correct version of tool x.

# Install

Plugin:

```shell
asdf plugin add arduino-cli
# or
asdf plugin add arduino-cli https://github.com/egnor/asdf-arduino-cli.git
```

arduino-cli:

```shell
# Show all installable versions
asdf list-all arduino-cli

# Install specific version
asdf install arduino-cli latest

# Set a version globally (on your ~/.tool-versions file)
asdf global arduino-cli latest

# Now arduino-cli commands are available
arduino-cli version
```

Check [asdf](https://github.com/asdf-vm/asdf) readme for more instructions on how to
install & manage versions.

# Contributing

Contributions of any kind welcome! See the [contributing guide](contributing.md).

[Thanks goes to these contributors](https://github.com/egnor/asdf-arduino-cli/graphs/contributors)!

# License

See [LICENSE](LICENSE) © [Daniel Egnor](https://github.com/egnor/)
