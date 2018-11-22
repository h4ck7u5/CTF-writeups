https://github.com/ctfs/write-ups-2015/tree/master/camp-ctf-2015/forensics/APT-incident-response-400

get an info of the dump file

```
$ volatility -f memorydump imageinfo

Volatility Foundation Volatility Framework 2.6
INFO    : volatility.debug    : Determining profile based on KDBG search...
          Suggested Profile(s) : No suggestion (Instantiated with LinuxDebian608x64)
                     AS Layer1 : LimeAddressSpace (Unnamed AS)
                     AS Layer2 : FileAddressSpace (/home/h4ck7u5/Downloads/ritsecCTF2018/bucketocash/memorydump)
                      PAE type : No PAE
                           DTB : -0x1L
```


$ strings -a memorydump | grep -iEo '(linux|ubuntu|debian|windows)' | sort | uniq -c | sort -n
      1 debian
      1 DEbian
      1 WINDOWS
      2 Debian
     34 windows
     36 Windows
    128 LINUX
    533 Linux
  16225 linux

$ strings -a memorydump  | grep -iEo '(hamm|slink|potato|woody|sarge|etch|lenny|squeeze|wheezy|jessie|stretch)' | sort | uniq -c | sort -n
      1 Hamm
      2 etCh
      4 hamm
      4 squeeze
      5 stretch
      8 ETCH
     14 STRETCH
    121 etch
