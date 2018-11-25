# copper gate
inspect the source code
```
<img src="images/banner.png" alt="banner" height="150" width="700">
```
... and navigate to the image path...here we find an interesting textfile

http://18.191.227.167/images/sitenotes.txt

Site is in development, but active updates can be viewed by going to **/devvvvv/index.html**

http://18.191.227.167/devvvvv/home.html

```bash
$ cat index.html
```
<meta http-equiv="refresh" content="0; URL='home.html'" />

```
<!-- Congratulations! You have discovered the path to the first flag. Please continue your journey at "**/enterthecoppergate/gate.html**" -->
```
```bash
$ curl http://18.191.227.167/enterthecoppergate/gate.html
```
```
				<h1>CONGRATULATIONS!</h1>
				<h2>You have found the Copper Flag.</h2>
				</br>
				<img src="copperkey.jpg" alt="Copper" height=272 width=640>
				</br>
				<p>
					<b>VFVDVEZ7VzNsYzBtM19UMF9UaDNfMDQ1MTVfVGgzX0MwcHAzcl9LM3l9Cg==</b>
```
```bash
$ echo VFVDVEZ7VzNsYzBtM19UMF9UaDNfMDQ1MTVfVGgzX0MwcHAzcl9LM3l9Cg== | base64 -d
```

**TUCTF{W3lc0m3_T0_Th3_04515_Th3_C0pp3r_K3y}**
