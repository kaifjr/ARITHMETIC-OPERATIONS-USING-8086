NAME : KAIF MOHAMED P 
REG NO : 212222043004

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
|                         |                          |
|      1201:34            |  68:1205                 |
|      1202:12            |  00:1206                 |
|      1203:34            |  c4:1207                 |                             
#### Manual Calculations

![WhatsApp Image 2025-09-14 at 19 05 55_96d7008d](https://github.com/user-attachments/assets/154132dd-d0e8-42bb-8798-5cb0ed283f7f)



## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="901" height="593" alt="Screenshot 2025-09-14 182139" src="https://github.com/user-attachments/assets/2a6ee828-4b7f-4a83-8650-138452df5eb4" />


<img width="916" height="593" alt="Screenshot 2025-09-14 175635" src="https://github.com/user-attachments/assets/ee533120-4050-4d87-8e57-b634b304935c" />


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

| MEMORY LOCATION (INPUT)  | MEMORY LOCATION (OUTPUT) |
| -----------------------  | ------------------------ |
|                          |                          |
|      1201:34             |  68:1205                 |
|      1202:12             |  00:1206                 |
|      1203:34             |  c4:1207                 |                            
#### Manual Calculations

![WhatsApp Image 2025-09-14 at 19 05 18_3d07f446](https://github.com/user-attachments/assets/e1b032f6-e76b-486a-8642-5f884d103ae2)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="893" height="587" alt="Screenshot 2025-09-14 182203" src="https://github.com/user-attachments/assets/90edbae7-11ca-4787-a938-8ad347753313" />

<img width="913" height="568" alt="Screenshot 2025-09-14 180909" src="https://github.com/user-attachments/assets/ca69b58d-f24a-4fa4-bf9c-d62735f6effa" />


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
|      1201:34            |   68:1205                |
|      1202:12            |   00:1206                |
|      1203:34            |   c4:1207                |                               
#### Manual Calculations
![WhatsApp Image 2025-09-14 at 19 04 26_d5ead66a](https://github.com/user-attachments/assets/ce6b9c66-f460-4df9-a438-0ee6a427d122)



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="885" height="587" alt="Screenshot 2025-09-14 182217" src="https://github.com/user-attachments/assets/dd1d9bdf-04c0-455f-b3d1-d15f3a67a645" />
<img width="904" height="566" alt="Screenshot 2025-09-14 183300" src="https://github.com/user-attachments/assets/ba532115-92a6-47d6-b064-c959d2002b31" />


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
|     1201:34             |  68:1205                 |
|    1202:12              | 00:1206                  |
|     1203:34             |  c4:1207                 |                                                               

#### Manual Calculations

![WhatsApp Image 2025-09-14 at 19 04 34_4e918cc8](https://github.com/user-attachments/assets/4d9b6322-8218-4170-963b-86c88be5a29d)


## OUTPUT FROM MASM SOFTWARE

<img width="921" height="576" alt="Screenshot 2025-09-14 182238" src="https://github.com/user-attachments/assets/d1b24a8e-d0a9-4486-9686-b860187c5fca" />
<img width="916" height="561" alt="Screenshot 2025-09-14 183450" src="https://github.com/user-attachments/assets/a3c592ae-be5b-4ab7-97f6-abe12a0bbcba" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
