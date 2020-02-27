## Bit Manipulation 

| Operator |  Use Case  | Explanation | Example | Status|
| --- | ----- | -------- | ---- | ----- |
|*AND*| `a & b`| if a == b == 1, then a & b = 1, otherwise = 0| `1 & 1 = 1`, `1 & 0 = 0`,`0 & 1 = 0`, `0 & 0 = 0 `| OK | 
|*OR*| `a \| b`| if a == 1 or b == 1, then `a \| b = 1`, otherwise = 0| `1 \| 1 = 1`, `1 \| 0 = 1`,`0 \| 1 = 1`, `0 \| 0 = 0 `| OK | 
|*XOR*| `a ^ b`| if a == 1 or b == 1, then a ^ b = 0, otherwise = 0| `1 ^ 1 = 0`, `1 ^ 0 = 1`,`0 ^ 1 = 1`, `0 ^ 0 = 0`| OK | 
|*NOT*| `- a`| inverse || AGAIN | 
|*LEFT MOVE*| `a << b`| `left shift` a ( in binary) b times |`9 << 2 = 36`| OK |
|*RIGHT MOVE*| `a >> b`| `right shift` a ( in binary) b times |`9 >> 2 = 2`, `-9 >> 2 = -3`| AGAIN | 
|*RIGHT MOVE AND ADD 0*| `a >>> b`| `right shift` a ( in binary) b times, remove out-of-boundry bit, and add 0 left |`19 >>> 2 = 4`| AGAIN | 


## Example 

- `15 & 9 = 9`   (1111 & 1001 = 1001) (bin(15) = 1111, bin(9) = 1001)
- `15 | 9 = 15`  (1111 | 1001 = 1111) (bin(15) = 1111, bin(9) = 1001)
- `15 ^ 9 = 6`  (1111 ^ 1001 = 0110) (bin(15) = 1111, bin(9) = 1001)
- `9 << 2 = 36` ( bin(9) = 1001, left shift 2 times -> 100100 ->  int('100100', 2) = 36)
- `9 >> 2 = 2` ( bin(9) = 1001, right shift 2 times -> 10 ->  int('10', 2) = 2)
- `-9 >> 2 = -3`  
- `19 >>> 2 = 4` ( bin(19) = 10001, right shift 2 times -> 100 -> add `0` make the length same as origin -> 00100 -> bin('100',2 )= 4)
- Minus : `0 -> 1`, `0 -> 1` then `add 1`
- `- (9)` : - (1001) -> (0110) + 1  -> `0111`
- `- (38)`  : - (00100110) -> (11011001) + 1 -> `11011010`


## Ref 
- https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Obsolete_Pages/Obsolete_Pages/Obsolete_Pages/%E9%81%8B%E7%AE%97%E5%AD%90/%E4%BD%8D%E5%85%83%E9%81%8B%E7%AE%97%E5%AD%90
- http://140.129.118.16/~richwang/99-2-Courses/About_C_BitOperation.pdf