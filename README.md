# MFSTOOL

Minix FileSystem Tool

This utility is used to manipulate Minix filesystem images in user-space.
It can be used to extract files and generate full images for using in
embedded system and/or Linux init ram disks.

Unlike mounting through Linux's mount device, this tool does not require
root priviledges and will allow regular users create device nodes on
the file system.

## install

```sh
autoconf
./configure
make
```

## usage

extract total filesystem to directory 'test'

```sh
mkdir test
./mfstool extract minixfs.bin test
```

extract one file:

```sh
./mfstool extract minixfs.bin /bin/busybox ./busybox_extract
```