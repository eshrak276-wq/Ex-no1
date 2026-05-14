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
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

<img width="900" height="621" alt="WhatsApp Image 2026-05-14 at 11 28 35 AM" src="https://github.com/user-attachments/assets/a4a5412b-3957-49df-ae72-9e666dbc4096" />


#### Manual Calculations

<img width="900" height="609" alt="WhatsApp Image 2026-05-14 at 11 28 46 AM" src="https://github.com/user-attachments/assets/ab64842c-1fea-4dba-9e81-f9a3ba82c916" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="900" height="1600" alt="WhatsApp Image 2026-05-14 at 11 27 27 AM" src="https://github.com/user-attachments/assets/0876e804-8fdb-48de-8227-5c874c2dffcc" />

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
<img width="900" height="726" alt="WhatsApp Image 2026-05-14 at 11 31 30 AM" src="https://github.com/user-attachments/assets/d62fb198-cd5d-4f77-93a8-441cf2886ea2" />


#### Manual Calculations

<img width="900" height="680" alt="WhatsApp Image 2026-05-14 at 11 31 44 AM" src="https://github.com/user-attachments/assets/e761e4d0-2cce-4384-abf8-09e704b295f3" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="900" height="1004" alt="WhatsApp Image 2026-05-14 at 11 32 28 AM" src="https://github.com/user-attachments/assets/4692101b-0cba-4aca-b782-694ae7358964" />

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

<img width="900" height="775" alt="WhatsApp Image 2026-05-14 at 11 32 59 AM" src="https://github.com/user-attachments/assets/77177411-e864-4d42-a856-bd4d30a3f0c9" />


#### Manual Calculations

<img width="897" height="691" alt="WhatsApp Image 2026-05-14 at 11 33 11 AM" src="https://github.com/user-attachments/assets/d1acb7bc-6b68-4897-8cc3-f46e1c25ff2a" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="900" height="1200" alt="WhatsApp Image 2026-05-14 at 11 33 21 AM" src="https://github.com/user-attachments/assets/cc4be229-6bbe-4515-a29b-a9e1e6569e0b" />

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

<img width="871" height="606" alt="WhatsApp Image 2026-05-14 at 11 34 47 AM" src="https://github.com/user-attachments/assets/eb13983c-e1f7-4e2c-a959-29e8f3343e35" />


#### Manual Calculations

<img width="900" height="769" alt="WhatsApp Image 2026-05-14 at 11 34 57 AM" src="https://github.com/user-attachments/assets/177c684c-398c-4272-8116-1dc9f173cebc" />



---
## OUTPUT FROM MASM SOFTWARE

<img width="1026" height="1137" alt="WhatsApp Image 2026-05-14 at 11 35 10 AM" src="https://github.com/user-attachments/assets/c384dcc1-21fc-4a8f-ba5f-2db70e25bacc" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

