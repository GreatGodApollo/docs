# Usage

```shell
$ lunar --help
    Lunar is a CLI for Spacebin that allows you to easily make documents.
    This application can be used in a couple of different ways
    to quickly create a document on an instance.
    
    You can either pipe a document into lunar by doing:
    'command | lunar'
    
    or upload a document directly:
    'lunar -f file.txt'
    
    Usage:
      lunar [flags]
    
    Flags:
          --config string       config file (default is $HOME/.lunar.yaml)
      -f, --file string         the file to upload
      -h, --help                help for lunar
      -i, --instance string     the spacebin instance (default "https://api.spaceb.in")
      -r, --raw                 do you want the raw url
          --result-url string   the base url for response (default "https://spaceb.in")
      -v, --version             version for lunar
```

`lunar` is pretty straight forward to use. You can either pipe a document into `lunar` by doing:
```shell
# *unix
$ cat file.txt | lunar

# Windows
$ type file.txt | lunar
```

or specify a document to upload:
```shell
$ lunar -f file.txt
```