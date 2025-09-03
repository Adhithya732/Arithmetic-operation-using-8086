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

| MEMORY LOCATION (INPUT)       | MEMORY LOCATION (OUTPUT) |
| -----------------------       | ------------------------ |
|          1200:  12            | 1204: 24                 |
|          1201:  34            | 1205: 68                 |
|          1202:  12            | 1206: 00                 |
|          1203:  34            |                          |
____________________________________________________________

#### Manual Calculations

<img width="1280" height="940" alt="image" src="https://github.com/user-attachments/assets/a8f19107-4b9c-454b-9a92-b671485ca49d" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="423" alt="image" src="https://github.com/user-attachments/assets/587d94a7-425d-4cbc-bbd0-bc9fdd3ab439" />

<img width="638" height="420" alt="image" src="https://github.com/user-attachments/assets/8239608e-460d-43b5-81ff-32192cde6ca2" />


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
code segment
assume cs:code,ds: code
org 1000h
mov si, 1200h
mov ax, [si]
mov bx, [si+02h]
mov c1,00h
sub ax, bx
jnc 11
inc cl
l1:mov[si+04h],ax
mov[si+06hl,cl
mov ah, 4ch
int 21h
code ends
end
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|        1200:12          | 1204:00                  |
|        1201:34          | 1205:00                  |
|        1202:12          | 1206:00                  |
|        1203:34          |                          | 
______________________________________________________

#### Manual Calculations

<img width="1280" height="814" alt="image" src="https://github.com/user-attachments/assets/7684923b-8875-4e14-b4c3-1228953fb437" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="433" alt="image" src="https://github.com/user-attachments/assets/36adde35-9d79-4211-ab91-f1e171b36c1b" />

<img width="638" height="425" alt="image" src="https://github.com/user-attachments/assets/69d08656-7203-45f8-868b-e4c3adb1c060" />




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
|  1200:12                | 1204:44                  |
|  1201:34                | 1205:51                  |
|  1202:12                | 1206:97                  |
|  1203:34                |                          |
______________________________________________________
#### Manual Calculations
<img width="1280" height="814" alt="image" src="https://github.com/user-attachments/assets/69207b21-9b79-4cd1-9197-de01fc252139" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="636" height="421" alt="image" src="https://github.com/user-attachments/assets/809f8a5c-0e2d-43d2-8697-ff2cad8ba3a7" />

<img width="640" height="425" alt="image" src="https://github.com/user-attachments/assets/8e321124-ec60-4d86-8fa8-ec598e5edc94" />

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
| 1200:12                 | 1204: 01                 |
| 1201:34                 | 1205: 00                 |
| 1202:12                 | 1206: 00                 |
| 1203:34                 |                          |
______________________________________________________
#### Manual Calculations

<img width="1280" height="674" alt="image" src="https://github.com/user-attachments/assets/00dceaad-9f78-42c0-93f8-0271791d841f" />


---
## OUTPUT FROM MASM SOFTWARE
<img width="647" height="430" alt="image" src="https://github.com/user-attachments/assets/4006e84a-4146-404f-9a2d-c1e2127cef95" />

<img width="637" height="431" alt="image" src="https://github.com/user-attachments/assets/4edc2df0-cdef-4b07-87eb-d7cc120d25c8" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
