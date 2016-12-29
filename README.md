# Playing with kubernetes 1.2.x

Tested on OSX 10.11.4

The starup.sh is the shell script that google ask you to curl-bash with small
changes.

## To start a new cluster on Virtualbox

First you have to export the variables in the env and then run the startup:

    $ source env.sh
    $ ./startup.sh

You can change the number of nodes, but 1 is not enough when using the default
virtualbox size.

## Changes in the startup file

I made two changes to the startup file (I downloaded the one they ask you to
curl-bash).

- First, now it WILL check if the file is already there and if it's there it won't
download it again.
- Second, it won't delete the archive when it ends the installation.

There is a problem with this approach. In case there is an update of kubernetes
the script won't download the new archive.

    Downloading kubernetes release v1.2.1 to ./kubernetes.tar.gz
    Found the tar.gz. I won't download it again!
    Unpacking kubernetes release v1.2.1

But you don't have this version! So just look at the shell when you start it ;)

## To destroy the VMs

From this directory:

    $ cd kubernetes
    $ vagrant destroy

## NOTES

- This specific script doesn't work with wmware_fusion as provider (their
  constraint).
- The .vagrant directory is save inside the kubernetes one.

## TODO

- Fix update problem (re-download only on update).
