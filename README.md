# sorting-of-numbers
## Aim
To write and execute an Assembly Language Program for sorting data in Ascending and  descending order using 8051 microcontroller on Keil software.
---

## Apparatus Required
- Personal Computer  
- Keil µVision software  
---

## Algorithm(ASCENDING ORDER)
1. Initialize the register **R7** with count (number of elements).  
2. Get the first two elements into two registers.  
3. Compare the two elements:  
   - If the value in register **R0** is lower, exchange **A** and **R0** data.  
   - Otherwise, increment pointer and decrement register **R7**.  
4. Check if **R7 = 0** → if yes, move the register **R0 & A**.  
5. Increment pointer and decrement **R7**.  
6. If **R7 ≠ 0**, repeat from Step 2.  
7. Otherwise, stop the program.  
---

## Program (Ascending order)

```
ORG 0000H
LOOP1:MOV R0,#40H
MOV R6,30H
DEC R6
LOOP:MOV A,@R0
CJNE A,B,NEXT
NEXT:JC DOWN
MOV@R0,A
DEC R0
INC R0
DOWN:DJNZ R6, LOOP
MOV R1,#02H
DJNZ R1,LOOP1
END

```
## OUTPUT(Ascending order)
<img width="722" height="384" alt="image" src="https://github.com/user-attachments/assets/43f84b45-4dc2-4098-8411-ee6990a65bf2" />



---

## Algorithm(Descending order)
1. Initialize the register **R7** with count.  
2. Get first two elements in two registers.  
3. Compare the two elements of data:  
   - If the value of **R0** register is high, then exchange **A** and **R0** data.  
   - Else, increment pointer and decrement register **R7**.  
4. Check if **R7 = 0**, then move the contents of **R0** and **A**.  
5. Again increment pointer and decrement **R7**.  
6. Check if **R7 = 0**:  
   - If **No**, repeat the process from Step 2.  
   - If **Yes**, stop the program.  
---
## Program (Descending order)

```
<img width="209" height="369" alt="image" src="https://github.com/user-attachments/assets/362731d1-1445-4f0d-a95a-30a1a2369577" />
```
## OUTPUT(Descending order)
<img width="722" height="447" alt="image" src="https://github.com/user-attachments/assets/d62bcbad-d59c-466f-983d-059bfae5a92a" />



---
## RESULT:
Thus the sorting of given data was done using 8051 keil software.

