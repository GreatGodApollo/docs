# Installation

To start it all off, you're going to need to install `lunar`, which can be done one of two ways, either by directly downloading the executable, or via `go get`

### Standard Download
If you don't have go installed, you can just head on over to the [releases](https://github.com/GreatGodApollo/lunar/releases) page and download the 
latest release for your platform. Extract it using something like [7-Zip](https://www.7-zip.org) for Windows or 
`tar` on other platforms (`tar -zxvf lunar*.tar.gz`).

That's it! Although you'll probably want to also add the binary to your path for ease of use.

### `go get`
If you **do** have go installed, you can just run a single command to install `lunar`:
```shell
$ go get -u github.com/GreatGodApollo/lunar
```