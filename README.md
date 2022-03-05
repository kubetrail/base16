# base16
encoder decoder in base16

## disclaimer
>The use of this tool does not guarantee security or suitability
for any particular use. Please review the code and use at your own risk.

## installation
This step assumes you have [Go compiler toolchain](https://go.dev/dl/)
installed on your system.

Download the code to a folder and cd to the folder, then run
```bash
go install
```

## usage
To encode pass input as arguments
```bash
base16 this is a test
7468697320697320612074657374
```

or pass input via STDIN
```bash
echo -n this is a test | base16
7468697320697320612074657374
```

> Pl. note that the STDIN is ignored if arguments are provided

To decode use flag `-d`
```bash
base16 -d 7468697320697320612074657374
this is a test
```

or pass input via STDIN
```bash
echo -n 7468697320697320612074657374 | base16 -d
this is a test
```

```bash
echo hello | base16 | base16 -d
hello
```
