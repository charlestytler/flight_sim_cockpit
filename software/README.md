# Software

## Build Instructions

To compile: `make <board_name>`

To upload: `make upload <board_name>-upload PORT=COM<#>`
> *Note: if PORT is not specified a warning will print available ports*

To monitor Serial output: `make monitor PORT=COM<#>`

## Prerequisites
Must have arduino-cli installed: https://arduino.github.io/arduino-cli/latest/

Makefiles have been set up to use arduino-cli installed in Windows (arduino-cli.exe) but can be executed from WSL linux bash.
