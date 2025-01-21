# Bit wise gates  

### And gate
- 0 0 | 0
- 0 1 | 0 
- 1 0 | 0
- 1 1 | 1

- Can be used for identifying power of 2 : 
- As power of 2 will have only 1 set bit 
- if it is a power then doing n & (n-1) will give zero

### OR gate
- 0 0 | 0
- 0 1 | 1
- 1 0 | 1
- 1 1 | 1

- Doing OR gate of two numbers will be a|b >=a if (a is greater than b) this also helps in retaining the state of previous number and adds the set bits of current number

### NOT gate (P.S representation of negative number )
- 0 | 1
- 1 | 0

### Negative number representation 
A negative number is represented as 2's compliment 
- for 2's compliment 
- convert all 0's to 1's and 1's to 0's
- Then add 1 to this compliment 
Example : 
- 1 in binary 32 bit is 0000...001
- For one's compliment it will be 111.....110
- For two's compliment it will be added with one : 111....111


### XOR gate 
- 0 0 | 0
- 0 1 | 1
- 1 0 | 1
- 1 1 | 1


### Left Shift (<<)
- it shifts the bit left side by the number of steps given eg (Number to apply on ) << (Bits to move) 3 << 1
- Ignore the values on left side and move up the values and add 0 in place of them
- 3 binary rep. is 000...011 , now left shifting will give 000...110 = 6

#### Note: shifting left side gives value X* 2^y (here X is the value we are shifting and Y is the times we are shifting ) As long as there is no over flow
eg: 6<<1 = 12 | (6*2^1)=12 

### Signed Right Shift (>>)
It makes sures if the number is positive it remains positive and if negative so on. (Number to apply on ) >> (Bits to move) 3 >> 1
- shifts bit to right ignores the bits on the right
- Adds 0 from left if positive or 1 if negative

- eg : 6>>1 :  000...110 , now right shift 000...011
- eg -6>>1 : 000..110 afters 1's compliment is 111...001 , add one now 111...010
- 111...010 is -6 now -6>>1 is 111...101 which on conversion is -3 (as 111..101 represents negative number)

#### Note: shifting left side gives value X % 2^y (here X is the value we are shifting and Y is the times we are shifting ) As long as there is no over flow
eg: 6>>1 = 3 | (6%2^1)=3 


### Unsigned Right shift (>>>)
- (Number to apply on ) >>> (Bits to move) 3 >>> 1
- 00...011 >> 1 00...001 = 1
- This effects negative numbers eg : -6 111...010 >>> 011..101 (this became a positive number 2147483645 ) 

