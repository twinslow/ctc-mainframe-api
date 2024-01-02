# MBRLIST entry format

1-8  d5c5e6e2d9c34040
       Member name = `NEWSRC  `

9    0f
       C byte from directory block entry  = 15 half words of user data

Byte 10 is where the ISPF stats information (user data) will start, if any.
## ISPF statistics entry

This is taken from this link: https://www.ibm.com/docs/en/zos/2.1.0?topic=di-ispf-statistics-entry-in-pds-directory

``` 
1-2    0100      VER=01 MOD=00 
3      00        FLAGS=00
4      57        MOD-TIME=57 
5-8    0123269f
       Creation date
       Century=01 (2000)
       Julian date=23269F (23.269)
9-12   0123269f
       Modification date
       Century=01 (2000)
       Julian date=23269F (23.269)
13-14  2307
       Modification time = 23:07 + MOD-TIME=57 from above.
15-16  0117      Current number of lines = 279
17-18  00F8      Initial number of lines = 248
19-20  0000      Number of modified lines = 0
21-27  c8c5d9c3 f0f140
       Modified user = `HERC01 ` (note 7 characters)
28-30  404040 (blank, bit 3 in 'C' flag was off)
       e700000000000000000000000000000000000000000000000000000000000000
```
