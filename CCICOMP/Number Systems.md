## Conversion Table
|        | Dec    | Bin            | Oct               | Hex                | Base m                  |
| ------ | ------ | -------------- | ----------------- | ------------------ | ----------------------- |
| Dec    | ~~/~~  | /2             | /8                | /16                | /m                      |
| Bin    | x2^pv  | ~~/~~          | split to 3 bits   | split by 4 bits    |                         |
| Oct    | x8^pv  | conv to 3 bits | ~~/~~             | oct to bin  to hex |                         |
| Hex    | x16^pv | conv to 4 bits | hex to bin to oct | ~~/~~              |                         |
| Base n | xn^pv  |                |                   |                    | base n to dec to base m |
Binary = 2 = 1-bit -> [0, 1]
Octal = 8 = 2 x 2 x 2 = 3-bits [0, 1, 2, 3, 4, 5, 6, 7,]
Hexadecimal = 16 = 2 x 2 x 2 x 2 = 4-bits
```Hexadecimal
10 = 0xA = 0x1010
11 = 0xB = 0x1011
12 = 0xC = 0x1100
13 = 0xD = 0x1101
14 = 0xE = 0x1110
15 = 0xF = 0x1111
```

###  Base to Dec:
$$
n\cdot Base^{(PV)}
$$
### Dec to Base:
$$
\frac{d}{Base}
$$
## Integer Representation
1. unsigned:
	1.  only (+)
	2. m = n -> all bits
	$$0 \rightarrow 2^n-1$$
	$$0 \rightarrow 2^8-1 \rightarrow[0 \rightarrow 255]$$
2. signed:
	1. (+) and (-)
	2. s = 1-bit
	3. m = n - 1
	$$-2^{n-1}\rightarrow2^{n-1}-1$$
	$$-2^{8-1}\rightarrow2^{8-1}-1\rightarrow[-128\rightarrow127]$$
#### Signed Integer

|         | s & m     | 1's C      | 2's C          |
| ------- | --------- | ---------- | -------------- |
| + s = 0 | m  = some | m = some   | m = some       |
| - s = 1 | m = some  | m = invert | m = invert + 1 |
#### Arithmetic
- 1's C -> add overflow
- 2's C -> truncate
#### Extension
- unsigned -> zero extensions
- signed -> sign extension
## Real Number Representation:
### IEEE 754 Standard
$$(-1)^s\cdot1.m\cdot2^E$$
- s - sign
	- if (+) -> s = 0
	- if (-) -> s = 1
- m - mantissa
- e - exponent
#### Single Precision
Float 32-bits
$$E'=E+127$$

| s     | E'     | m       |
| ----- | ------ | ------- |
| 1-bit | 8-bits | 23-bits |
#### Double Precision
double float 64-bits
$$E'=E+1023$$

| s     | E'      | m       |
| ----- | ------- | ------- |
| 1-bit | 11-bits | 52-bits |
