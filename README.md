# Zadaca3-8085

Да се проектира решение за раскрсница со помош на
семафори, да се предложи минимално хардверско решение
(како име на компонента). 


![Screenshot (1)](https://github.com/Ristova123/Zadaca3-8085/blob/main/Diagram.png)s


**Resenie:**

![Screenshot (2)](https://github.com/Ristova123/Zadaca3-8085/blob/main/Logika%20na%20semafori.png)


```
START MVI H,LIGHT

MVI L, LOC ;можеше и LXI H, LIGHT LOC

MOV A,M ; се вчитува првата локација од ROM

OUT PORTA ; се праќа на соодветна I/O порта

CALL DOCNI_1MIN ;се повикува процедура за доцнење од 1 минута

INX H ; зголеми го HL парот за 1 (наредна локација)

MOV A,M ; се вчитува втората локација од ROM

OUT PORTA ; се праќа на соодветна I/O порта

CALL DOCNI_3SEC ;се повикува процедура за доцнење од 3 секунди

-

-

MOV A,M ; се вчитува првата локација од ROM

OUT PORTA ; се праќа на соодветна I/O порта

CALL DOCNI_3SEC ;се повикува процедура за доцнење од 3 секунди

JMP START ;на почеток на првобитната состојба на семафорот

END 


```
**Develop by:**

[Tamara Ristova ](https://github.com/Ristova123)


**Subject**

Microcomputer's systems

**Built With**

This project is built using the following tools:

- [e8085](https://emu8086-microprocessor-emulator.en.softonic.com/): Assembler and emulator for the Intel 8085 microprocessor.

**Getting Started**

To get a local copy up and running, follow these steps.

**Prerequisites**

In order to run this project you need:

A working computer
Connection to internet
Setup

**How to Run**

To run the program, you need an 8085 emulator or assembler. You can use emulators like DOSBox or TASM (Turbo Assembler). Here's how to run the program using e8085.exe:

1. Download and install e8085.exe from [here](https://emu8086-microprocessor-emulator.en.softonic.com/).
2. Clone this repository to your local machine.
3. Open e8085.exe and load the `Semafor code.asm` file.
4. Assemble the code by pressing the Assemble button.
5. Run the program by pressing the Run button or by pressing F10.
