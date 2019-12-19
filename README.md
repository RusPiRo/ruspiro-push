# RusPiRo Push

This `cargo` tool allows to push new RuspiRo kernel images to the Rapsberry Pi assuming the receiving
bare metal kernel [Bootloader](https://www.github.com/RuspiRo/loader) is running there and it is
connected through a serial port to the development machine.

## Install
Use `cargo` to install this subcommand:
```
$> cargo install cargo-ruspiro-push
```

Once done you could call the tool like so:
```
$> cargo ruspiro-publish -k <image_file> -p <serial_port>
```

```console
$> cargo help ruspiro-push
Push Kernel to RPi 0.0.1
André Borrmann <pspwizard@gmx.de>
Send kernel files to raspberry Pi running RusPiRo Bootloader

USAGE:
    cargo-ruspiro-push.exe [OPTIONS] --kernel <FILENAME> --port <PORT_NAME> [ruspiro-push]

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

OPTIONS:
    -a, --aarch <32 | 64>      Kernel architecture mode 32 for aarch32 or 64 for aarch64
    -k, --kernel <FILENAME>    Kernel filename (+path) to be uploaded to RPi
    -p, --port <PORT_NAME>     Serial Port Name to use for communication (e.g. 'COM5' on Windows machine)

ARGS:
    <ruspiro-push>
```

## License
Licensed under Apache License, Version 2.0, ([LICENSE](LICENSE) or http://www.apache.org/licenses/LICENSE-2.0)