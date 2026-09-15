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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200🔢       01         12

|         1200                    |

#### Manual Calculations
<img width="1280" height="578" alt="492010962-22d0dde6-4892-41c9-8666-201fa546f89f" src="https://github.com/user-attachments/assets/530bba54-4bcb-4286-9d80-2562f290fa7e" />

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="662" height="433" alt="492011000-b3f2e067-6fa3-4685-8c5a-6ddbcabe8f58" src="https://github.com/user-attachments/assets/07c9c3c3-8326-4b13-9948-e865b1168649" />


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
|                         |                          |

#### Manual Calculations
<img width="578" height="1280" alt="492011031-9bb2ce6e-8393-4910-83cc-86ce0669bc9b" src="https://github.com/user-attachments/assets/6f78d0e9-fe3f-485b-b389-5aa0584f033b" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="635" height="426" alt="492011107-a9b6c1f4-8504-4b62-a46b-45f2c9f73e7c" src="https://github.com/user-attachments/assets/eb9bdb73-d786-4863-8797-b9144317eb9a" />


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
|                         |                          |

#### Manual Calculations

<img width="1280" height="578" alt="492011213-6fd6893e-c61e-44b1-84ad-8f233dc40885" src="https://github.com/user-attachments/assets/85065e08-7d0b-476f-9a48-1982b75463db" />
---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="627" height="444" alt="492011250-ca85eb30-b06c-4500-a468-041e1549c46c" src="https://github.com/user-attachments/assets/60eb3015-1b6e-4cf9-b501-89a6f555b653" />


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
|                         |                          |

#### Manual Calculations

<img width="1280" height="578" alt="492011258-f58946bb-9637-47c6-b644-21a5470f45b7" src="https://github.com/user-attachments/assets/c729605c-e23a-4016-bcea-ea5d40652fab" />
---
## OUTPUT FROM MASM SOFTWARE
<img width="645" height="430" alt="492011294-8de04198-3de3-48f1-9c44-7554b86d1ef3" src="https://github.com/user-attachments/assets/32d625dc-4cca-4224-9624-de9a583418ee" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

