# INim: interactive shell (REPL)
![Nim CI](https://github.com/inim-repl/INim/workflows/Nim%20CI/badge.svg)

```
nimble install inim
```

<img width="721" alt="Screenshot 2024-06-28 at 18 33 47" src="https://github.com/inim-repl/INim/assets/1467605/523c973b-ca2c-450e-92f2-187e2e580be0">

## Features

* Runs on Linux, macOS and Windows
* Auto-indent (`if`, `for`, `proc`, `var`, ...)
* Arrow keys support (command history and line navigation)
* Prints out value and type of discarded expressions: ```>>> x```
* Uses current `nim` compiler in PATH
* Runs in the current directory: `import` your local modules (access to exported* symbols)
* Preload existing source code (access to non-exported* symbols): `inim -s example.nim`
* Optional Colorized output
* Edit lines using $EDITOR (Ctrl-X)
* Built in tools like ipython (cd(), ls(), pwd(), call()) enabled with `--withTools`
* When piped a file or some code, INim will execute that code and exit
* Extra compiler options can be specified by adding them as arguments inim with the -d flag (ie `inim -d:ssl -d:DEBUG`)
* Flags can turned on with `-d` by adding a `--` prefix to arguments (ie -d:--threads:on)

## Configuration

`inim --createRcFile`, for persistent configuration which is loaded from these locations:

* Linux & macOS: `~/.config/inim`
* Windows: `%APPDATA%\inim`

The config allows you to change the defaults for:

* Style
  * `prompt`: Set prompt string (default: "inim> ")
  * `showTypes`: Show var types when printing without echo (default: true)
  * `showColor`: Output results with pretty colors
* History
  * persistent history (default: true)
* Features
  * `withTools`: Enable built in tools

## Contributing

Pull requests and suggestions are welcome.

![alt text](https://github.com/AndreiRegiani/INim/blob/master/readme.gif?raw=true)
