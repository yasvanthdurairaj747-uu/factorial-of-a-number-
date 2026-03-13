
## FACTORIAL OF A NUMBER USING 8051 (Keil)

### AIM
To write and execute an Assembly Language Program to perform the factorial of a number using 8051 Keil.


### APPARATUS REQUIRED
- Personal computer with Keil software

### ALGORITHM
1. **Start**
2. **Input**: Read the number `n`.
3. **Initialize**:
   - Set factorial to `1`.
   - Set `i` to `1`.
4. **Loop**: While `i` is less than or equal to `n`:
   - Multiply factorial by `i`.
   - Increment `i` by `1`.
5. **Output**: Store or print the value of factorial.
6. **End**

---

### FLOWCHART
<img width="406" height="325" alt="image" src="https://github.com/user-attachments/assets/f3b47187-6f0f-490c-8704-f2973cb2b276" />

---

### PROGRAM
```asm
ORG 0000H
MOV DPTR,#4500H
MOVX A,@DPTR
MOV R0,A
INC DPTR
ACALL FACTORIAL
MOVX @DPTR,A
SJMP THIN
FACTORIAL:DEC R0
CJNE R0,#01H,PRODUCT
SJMP THICK
PRODUCT:MOV B,R0
MUL AB
ACALL FACTORIAL
THICK: RET
THIN:RET
END

```
### OUTPUT

<img width="972" height="589" alt="image" src="https://github.com/user-attachments/assets/918bed55-10fc-48ca-9e79-b9745fb44678" />


### MANUAL CALCULATION
![WhatsApp Image 2026-02-26 at 08 16 46](https://github.com/user-attachments/assets/d8db3ada-9057-43fe-a613-2bc0e3cda750)



### RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---
