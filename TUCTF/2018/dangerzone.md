## dangerzone

first we run strings to see the functions
```
$ strings dangerzone.pyc
```
./dangerzone.pyt
**reverse**
base64t
**b32decode(**
./dangerzone.pyR
./dangerzone.pyt
reversePigLatin
**rot13(**
decode(
./dangerzone.pyR
Something Something Danger Zones(
**=YR2XYRGQJ6KWZENQZXGTQFGZ3XCXZUM33UOEIBJ(**

... seems like a reversed base32

```
echo '=YR2XYRGQJ6KWZENQZXGTQFGZ3XCXZUM33UOEIBJ' | rev | base32 -d | rot13 -d
```
put it in the right order
```
$ echo -e "str='UCTF{r3d_l1n3_0v3rl04d}T';print(str[-1::]+str[0:-1:])" | python
TUCTF{r3d_l1n3_0v3rl04d}
```

**TUCTF{r3d_l1n3_0v3rl04d}**
