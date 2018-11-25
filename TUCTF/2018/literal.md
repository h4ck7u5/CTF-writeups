# literal

page is redirecting to wikipedia, so pull the source with wget
```bash
$ wget http://18.222.124.7
```
--2018-11-24 00:35:20--  http://18.222.124.7/
Connecting to 18.222.124.7:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 95 [text/html]
Saving to: ‘index.html’

**index.html**                         100%[================================================================>]      95  --.-KB/s    in 0s

2018-11-24 00:35:21 (5.11 MB/s) - ‘index.html’ saved [95/95]

```bash
$ cat index.html
```

```html
<html>

<head>
	<meta http-equiv="refresh" content="0; URL='Literal.html'" />
</head>

</html>
```

```bash
$ wget http://18.222.124.7/Literal.html
```
--2018-11-24 00:35:54--  http://18.222.124.7/Literal.html
Connecting to 18.222.124.7:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 841 [text/html]
Saving to: ‘Literal.html’

Literal.html                       100%[================================================================>]     841  --.-KB/s    in 0s

2018-11-24 00:35:55 (63.4 MB/s) - ‘Literal.html’ saved [841/841]

```bash
$ cat Literal.html
```
```html
<html>
  <head>
  <meta http-equiv="Refresh" content="1; url=https://en.wikipedia.org/wiki/Fork_bomb">
  </head>
  <body>
  <!--
        *   *                     f   f   f
      *  ** *                   ff  ff  ff
      * * ** ||                ff  ff  ff
    **   ||||T||              fUffffffff
      *   |C|||T| oooooooooooo fFff
           |||||||{ooooooooooRfff3o
          ooo4ooooooooooooooLff.ooooo0
        oooNooooooooooooooo3ooooooo5ooo.
        oooo4oooooRoooooooooo3oooooooooo.
        oooDooooo4oooooNooooooooooooooooo
        ooooooooooooooGoooooooooooooooooo
        ooooooooooooooooooooo3oooooooooRo
         oooooooo0oooooooooooooooooooooo
          oooooooffUoooooooooooooooooo
            ooofff5ooooooooooooooooo
             fff }ooooooooooooooo
            fff
  -->
  Redirecting to Wikipedia...!
  </body>
</html>

```
look closely at the bomb to retrieve the flag

***TUCTF{R34L.0N35.4R3.D4NG3R0U5}***
