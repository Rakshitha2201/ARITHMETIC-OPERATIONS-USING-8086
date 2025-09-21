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
| 2000  |  79    |
| 2001  |  88    |
| 2002  |  23    |
| 2003  |  02    |

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 2004  |  9C    |
| 2005  |  8A    |
| 2006  |  00    |

#### Manual Calculations

![WhatsApp Image 2025-09-21 at 10 55 15 PM](https://github.com/user-attachments/assets/c4902008-7223-4097-8377-8522bc47a3f2)


## OUTPUT IMAGE FROM MASM SOFTWARE

![WhatsApp Image 2025-09-21 at 9 39 21 PM](https://github.com/user-attachments/assets/6a070e7f-87d8-49e4-9c6c-6d0a7f92bdd6)


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
| 2000  |  79    |
| 2001  |  88    |
| 2002  |  23    |
| 2003  |  02    |

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 2004  |  56    |
| 2005  |  86    |
| 2006  |  00    |

#### Manual Calculations

![WhatsApp Image 2025-09-21 at 10 55 16 PM](https://github.com/user-attachments/assets/d8e79f8a-5131-4d75-b1d7-fc5123f01f5f)



## OUTPUT SCREEN FROM MASM SOFTWARE

![WhatsApp Image 2025-09-21 at 9 39 50 PM](https://github.com/user-attachments/assets/09cc7020-7447-4801-808e-58f6d128c7b6)


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
| 2000  |  02    |
| 2001  |  00    |
| 2002  |  03    |
| 2003  |  00    |

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 2004  |  06    |
| 2005  |  00    |
| 2006  |  00    |


#### Manual Calculations

![WhatsApp Image 2025-09-21 at 10 55 16 PM (1)](https://github.com/user-attachments/assets/8f39c4e8-de9e-4d21-beae-3b9024968655)

## OUTPUT SCREEN FROM MASM SOFTWARE

![WhatsApp Image 2025-09-21 at 9 39 35 PM](https://github.com/user-attachments/assets/0f9a9fba-29d7-4e2f-adc6-8ef81f3b4059)


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
| 2000  |  69    |
| 2001  |  24    |
| 2002  |  23    |
| 2003  |  12    |

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 2004  |  02    |
| 2005  |  00    |
| 2006  |  01    |

#### Manual Calculations

![WhatsApp Image 2025-09-21 at 10 55 17 PM](https://github.com/user-attachments/assets/788a1773-f7b3-45ee-a818-c3baffafc7cb)

## OUTPUT FROM MASM SOFTWARE

![WhatsApp Image 2025-09-21 at 9 39 09 PM](https://github.com/user-attachments/assets/e76170b0-e01a-4c0a-ab84-800b057def8e)




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

