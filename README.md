# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2000                   |   79                     | 
|  2001                   |   88                     |
|  2002                   |   23                     |
|  2003                   |   02                     |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2004                   |   56                     | 
|  2005                   |   86                     |
|  2006                   |   00                     |
#### Manual Calculations

<img width="789" height="849" alt="image" src="https://github.com/user-attachments/assets/473999b9-3cbf-4290-9851-31258afdf5ca" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE


![WhatsApp Image 2025-09-21 at 23 08 15_07c20e5f](https://github.com/user-attachments/assets/0e0486ad-c530-4e14-9405-feb4d6cbc470)

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2000                   |   79                     | 
|  2001                   |   88                     |
|  2002                   |   23                     |
|  2003                   |   02                     |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2004                   |   56                     | 
|  2005                   |   86                     |
|  2006                   |   00                     |
#### Manual Calculations

<img width="519" height="650" alt="image" src="https://github.com/user-attachments/assets/426bdf33-a45d-4ec9-b80f-222f9c9244f1" />

---


## OUTPUT SCREEN FROM MASM SOFTWARE


![WhatsApp Image 2025-09-21 at 23 08 16_e7782c23](https://github.com/user-attachments/assets/b768a9fa-c062-407f-94a6-c7a6edf667f4)

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2000                   |   02                     | 
|  2001                   |   00                     |
|  2002                   |   03                     |
|  2003                   |   00                     |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2004                   |   06                     | 
|  2005                   |   00                     |
|  2006                   |   00                     |

#### Manual Calculations

<img width="581" height="587" alt="image" src="https://github.com/user-attachments/assets/12118b7e-8d7e-4927-91ce-f0e4d5d0c6a6" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE


![WhatsApp Image 2025-09-21 at 23 08 16_6693a9a1](https://github.com/user-attachments/assets/8f61cdf3-96c4-4b43-86dc-281ca99d3947)

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2000                   |   69                     | 
|  2001                   |   24                     |
|  2002                   |   34                     |
|  2003                   |   12                     |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2004                   |   02                     | 
|  2005                   |   00                     |
|  2006                   |   01                     |
#### Manual Calculations

<img width="501" height="601" alt="image" src="https://github.com/user-attachments/assets/52e31649-40c6-4c74-a9af-65f9248456a0" />

---
## OUTPUT FROM MASM SOFTWARE

![WhatsApp Image 2025-09-21 at 23 08 17_c1fadf8a](https://github.com/user-attachments/assets/805b99f4-3d5c-404d-8b14-1262a3353109)




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

