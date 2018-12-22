```
$ foremost -v classified_gift_distribution_schema.img
```
Foremost version 1.5.7 by Jesse Kornblum, Kris Kendall, and Nick Mikus
Audit File

Foremost started at Thu Dec 20 21:32:15 2018
Invocation: foremost -v classified_gift_distribution_schema.img
Output directory: /home/h4ck7u5/Downloads/xmasctf/2018/message_from_santa/output
Configuration file: /etc/foremost.conf
Processing: classified_gift_distribution_schema.img

File: classified_gift_distribution_schema.img
Start: Thu Dec 20 21:32:15 2018
Length: 10 MB (10485760 bytes)

Num	 Name (bs=512)	       Size	 File Offset	 Comment

0:	00003184.jpg 	     109 KB 	    1630208 	 
1:	00000080.png 	       4 KB 	      40960 	  (273 x 187)
2:	00000092.png 	       3 KB 	      47104 	  (273 x 187)
3:	00000100.png 	      33 KB 	      51200 	  (273 x 273)
4:	00000168.png 	      45 KB 	      86016 	  (273 x 273)
5:	00000260.png 	       4 KB 	     133120 	  (273 x 273)
6:	00000272.png 	      24 KB 	     139264 	  (273 x 273)
7:	00000324.png 	      40 KB 	     165888 	  (273 x 273)
8:	00000408.png 	     105 KB 	     208896 	  (273 x 273)
9:	00000620.png 	       8 KB 	     317440 	  (273 x 187)
10:	00000640.png 	      70 KB 	     327680 	  (273 x 273)
11:	00000784.png 	      35 KB 	     401408 	  (273 x 273)
12:	00000856.png 	      51 KB 	     438272 	  (273 x 273)
13:	00000960.png 	      45 KB 	     491520 	  (273 x 273)
14:	00001052.png 	      71 KB 	     538624 	  (273 x 273)
15:	00001196.png 	     101 KB 	     612352 	  (273 x 273)
16:	00001400.png 	      49 KB 	     716800 	  (273 x 273)
17:	00001500.png 	      75 KB 	     768000 	  (273 x 273)
18:	00001652.png 	       5 KB 	     845824 	  (273 x 273)
19:	00001664.png 	      40 KB 	     851968 	  (273 x 273)
20:	00001748.png 	      45 KB 	     894976 	  (273 x 273)
21:	00001840.png 	      67 KB 	     942080 	  (273 x 273)
22:	00001976.png 	      25 KB 	    1011712 	  (273 x 273)
23:	00002028.png 	      79 KB 	    1038336 	  (273 x 273)
24:	00002188.png 	      58 KB 	    1120256 	  (273 x 273)
25:	00002308.png 	      950 B 	    1181696 	  (273 x 273)
26:	00002312.png 	      33 KB 	    1183744 	  (273 x 273)
27:	00002380.png 	      88 KB 	    1218560 	  (273 x 273)
28:	00002560.png 	      55 KB 	    1310720 	  (273 x 273)
29:	00002672.png 	       3 KB 	    1368064 	  (273 x 187)
30:	00002680.png 	      92 KB 	    1372160 	  (273 x 273)
31:	00002868.png 	      79 KB 	    1468416 	  (273 x 273)
32:	00003028.png 	      61 KB 	    1550336 	  (273 x 273)
33:	00003152.png 	       3 KB 	    1613824 	  (273 x 187)
34:	00003160.png 	       3 KB 	    1617920 	  (273 x 187)
35:	00003168.png 	       6 KB 	    1622016 	  (273 x 187)

Finish: Thu Dec 20 21:32:15 2018

36 FILES EXTRACTED

jpg:= 1  
png:= 35

Foremost finished at Thu Dec 20 21:32:15 2018

append the images to one file

```
$ convert +append ./output/png/*.png OUT.png
```
... install gaps to solve the puzzle and get the image-size with exiftool

```
$ exiftool ./output/png/00000080.png | grep -i "width"
```
Image Width                     : **273**  
Virtual Image Width             : 1913

```
$ gaps --image=OUT.png --generations=20 --population=600 --size=273
```
... finally read the flag from the image :-)

**X-MAS{1t_l00k5_l1k3_s4nta_m4de_4_m1stak3_sorry}**
