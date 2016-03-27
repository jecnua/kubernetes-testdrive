#

# Changes

There are 3 main changes. The first one is that I enforce the provider (I
changed shell once and it was trying to use gce -,-)

    export VAGRANT_DEFAULT_PROVIDER=virtualbox
    export KUBERNETES_PROVIDER=vagrant

Second is that it WILL check if the file is there (if it's there it won't
download it again).

Third it won't delete the archive (or point two makes no sense).

## NOTES
wmware_fusion doesn't work
