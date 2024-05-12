<div align="center">

# asdf-arduino-cli [![Build](https://github.com/egnor/asdf-arduino-cli/actions/workflows/build.yml/badge.svg)](https://github.com/egnor/asdf-arduino-cli/actions/workflows/build.yml) [![Lint](https://github.com/egnor/asdf-arduino-cli/actions/workflows/lint.yml/badge.svg)](https://github.com/egnor/asdf-arduino-cli/actions/workflows/lint.yml)

[arduino-cli](https://github.com/arduino/arduino-cli) plugin for
[asdf](https://asdf-vm.com) and [mise](https://mise.jdx.dev/). This plugin
is NOT maintained or supported by the Arduino project.

</div>

# Contents

- [Dependencies](#dependencies)
- [Install](#install)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

# Dependencies

- `bash`, `curl`, `tar`, and [POSIX utilities](https://pubs.opengroup.org/onlinepubs/9699919799/idx/utilities.html).

# Install

Plugin:

```shell
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

See [asdf](https://asdf-vm.com/guide/getting-started.html)
and/or [mise](https://mise.jdx.dev/getting-started.html) documentation
for more on installing and managing versions.

# Configuration

By default, `arduino-cli` stores configuration and cache files in
`~/.arduino15` and sketches in `~/Arduino`. If you're using a version
manager you probably want something more hermetic; consider setting
`$ARDUINO_DIRECTORIES_DATA`, `$ARDUINO_DIRECTORIES_USER`,
`$ARDUINO_CONFIG_FILE`, and/or
[other variables](https://arduino.github.io/arduino-cli/0.35/configuration/)
to local project-specific directories.

If you're using mise, you can put something like this in `.mise.toml`:

```toml
[env]
ARDUINO_DIRECTORIES_DATA = "{{config_root}}/arduino_data"
ARDUINO_DIRECTORIES_USER = "{{config_root}}/arduino_user"
ARDUINO_CONFIG_FILE = "{{config_root}}"
```

You'd likely want `arduino_data/` in `.gitignore`.

Note that `$ARDUINO_CONFIG_FILE` [points to a directory, not the config file
itself](https://github.com/arduino/arduino-cli/issues/753);
the actual file must be named `arduino-cli.{yaml,toml,json,...}`.

# Contributing

Contributions of any kind are welcome! See the [contributing guide](contributing.md).

# License

See [LICENSE](LICENSE) © [Daniel Egnor](https://github.com/egnor/)
