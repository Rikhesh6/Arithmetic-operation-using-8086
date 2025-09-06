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
MOV SI,1200H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200=12|1204=24|
| 1201=34                     
| 1202=12|1205=68|
| 1203=34| 
#### Manual Calculations

![WhatsApp Image 2025-09-06 at 12 27 19_717a6960](https://github.com/user-attachments/assets/8c0c75d2-b7e7-498c-8ccc-43795f591cc8)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="626" height="389" alt="image" src="https://github.com/user-attachments/assets/66a26b7f-e3ea-4c6a-b2aa-2555d0cb8c1d" />

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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 2000=24|   2004=12                       |
|2001=68|
|2002=12|2005=34|
|2003=34|
#### Manual Calculations

![WhatsApp Image 2025-09-06 at 12 27 18_b2af6e47](https://github.com/user-attachments/assets/faf601e7-0137-4070-abf9-40d359007b49)


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="622" height="394" alt="image" src="https://github.com/user-attachments/assets/a0d634ab-79c3-4995-8b02-445bc6e9806b" />

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
 2000=12|   2004=44                      |
|2001=34|2005=51|
|2002=12|2006=97|
|2003=34|  2007=0A                        |

#### Manual Calculations

![WhatsApp Image 2025-09-06 at 12 27 21_0bba13e0](https://github.com/user-attachments/assets/6a79f46e-5461-45eb-b82f-6f703a711181)


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="398" alt="image" src="https://github.com/user-attachments/assets/fdc5ff8c-6020-40ce-971a-b92bb27bb871" />

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
 2000=24|   2004=02                     |
|2001=68|2005=00|
|2002=12|2006=00|
|2003=34|  2007=00                    |

#### Manual Calculations

![WhatsApp Image 2025-09-06 at 12 27 20_36015d75](https://github.com/user-attachments/assets/7f51e01e-0d36-43ae-8820-c1a10bc76033)


---
## OUTPUT FROM MASM SOFTWARE
<img width="627" height="399" alt="image" src="https://github.com/user-attachments/assets/35753395-48f2-4b80-bd96-c3d0f2556fdc" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
