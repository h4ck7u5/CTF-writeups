## yeahright

download both files and run strings on binary

```bash
$ strings yeahright
AUATL
[]A\A]A^A_
7h3_m057_53cr37357_p455w0rd_y0u_3v3r_54w
*Ahem*... password?
yeahright!
/bin/cat ./flag
```
check the local flag file
```bash
$ cat flag
flag{test-flag-here}
```
... lets try the password found above
```bash
$ ./yeahright
*Ahem*... password? 7h3_m057_53cr37357_p455w0rd_y0u_3v3r_54w
flag{test-flag-here}
```
... the password is correct so the flag file gets read
```bash
$ nc 18.224.3.130 12345
*Ahem*... password? 7h3_m057_53cr37357_p455w0rd_y0u_3v3r_54w
TUCTF{n07_my_fl46_n07_my_pr0bl3m}
```
**TUCTF{n07_my_fl46_n07_my_pr0bl3m}**
