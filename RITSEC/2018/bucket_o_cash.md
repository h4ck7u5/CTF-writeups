# bucket o cash
identify file type first
```bash
file memorydump
memorydump: data
```
get head of the file in hex to define the filetype
```bash
xxd memorydump | head
00000000: 454d 694c 0100 0000 0010 0000 0000 0000  EMiL............
00000010: ffeb 0900 0000 0000 0000 0000 0000 0000  ................
00000020: 0000 0000 0000 0000 0000 0000 0000 0000  ................
```
its a Volatility file

search for operating system of memorydump

```bash
$ strings memorydump | grep "Linux version"

   Linux version 3.10.0-862.el7.x86_64 (builder@kbuilder.dev.centos.org) (gcc version 4.8.5 20150623 (Red Hat 4.8.5-28
```
