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

The target architecture will be derived from the filename. `kernel7.img` will be handled as Aarch32
and `kernel8.img` will handled as Aarch64 target. For any other file name you need to provide the 
desired target architecture of the kernel file to be transfered using the `-a` flag. Use the
`--help` flag to see all available options for this command:
```
$> cargo ruspiro-push --help
Push a kernel image to Raspberry Pi 0.1.0
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