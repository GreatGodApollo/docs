# Usage

```shell
$ genday --help
    Usage: genday [--version] [--verbose] COMMAND [arg...]

    Generate a curday.dat file

    Options:
    -v, --version   Show the version and exit
    -V, --verbose   Verbose debug mode

    Commands:
    json            generate a file from JSON

    Run 'genday COMMAND --help' for more information on a command.
```

`genday` is pretty straight forward to generate a `curday.dat` from a JSON file:
```
$ genday json input.json -o output.dat
    [GD] Successfully saved to output.dat
    [GD] Generated X listings
```

To learn more about this JSON format, [read on](./format.md).