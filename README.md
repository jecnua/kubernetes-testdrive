# Playing with kubernetes 1.2

## Usage

First you have to export the variables in the env and then run the startup:

    source env.sh
    ./startup.sh

## Changes in the startup file

I made two changes to the startup file.
First, now it WILL check if the file is already there and if it's there it won't
download it again.

Second, it won't delete the archive when it ends the installation.

## NOTES

- This specific script doesn't work with wmware_fusion as provider.
- The .vagrant directory is save inside the kubernetes one.
