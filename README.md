# 4bit-RCA-180nm-Layout
Layout of 4bit Ripple Carry Adder (RCA) formed using CMOS logic in gpdk180nm technology node done in Cadence Virtuoso with no DRC and LVS errors. 


## 4bit Ripple Carry Adder (RCA)
A 4-bit Ripple Carry Adder (RCA) is formed using four 1-bit Full Adders cascaded in a series connection with the Carry out of one stage acting as Carry in to another stage. A 4-bit Ripple Carry Adder (RCA) is used to calculate the binary addition of two 4bit binary numbers.
Since it is made using four 1-bit Full Adders, a 4-bit RCA has 8 inputs namely (A0 B0,………A3B3) and 4 Sum outputs namely (S0,…..S3) and a single Carry in as (Cin) to the
adder at first stage and a single Carry out as (Cout) from the final stage in the adder chain <br>

![image](https://github.com/user-attachments/assets/5292df55-6fd6-46d1-87c7-7d8ae46b46c7) <br> Fig 1: Adding two 4bit numbers. <br><br>

## Ripple Carry Adder formed using CMOS logic
Since we know that, to form a 4bit RCA we require four 1bit Full Adders. To make Full Adders we require Half Adders. Furthermore Half Adders can be made with simple Logic Gates. In this section, I will be showing how to make these components leading upto a 4bit RCA in gpdk 180nm technology node using CMOS logic.

### Half Adder

A half adder is a simple digital circuit used to add two binary numbers. It contains two outputs, namely Carry (C) and Sum (S), and two inputs, as A and B, denoting the two bits to be added.
XOR and AND gates are two common logic gates that can be used to create the half adder. <br>

![image](https://github.com/user-attachments/assets/12ad78a0-94bd-4697-b044-9dc956e90028) <br> Fig 2: Boolean Expression for Sum and Carry output of a Half Adder. <br><br>
![image](https://github.com/user-attachments/assets/3c9a649e-ffac-4c3f-ab4c-03747f591513) <br> Fig 3: Truth Table of a Half Adder. <br><br>
![HA](https://github.com/user-attachments/assets/1c158054-f657-4c8f-b2f1-859395f29914) <br> Fig 4: Schematic of a Half Adder. <br><br>

### 1bit Full Adder

A 1-bit Full Adder is formed using two Half Adders cascaded in series with each other and an OR gate. It takes in three 1-bit inputs namely A, B, Cin and performs the binary addition to
give Sum and Carry output (Cout) from these three bits. <br>

![image](https://github.com/user-attachments/assets/45e3b1c7-bd34-492c-aa0a-45aad872e525) <br> Fig 5: Boolean Expression for Sum output of a 1bit Full Adder. <br><br>
![image](https://github.com/user-attachments/assets/6b474823-9ec4-47ee-b4ad-119e486bccd3) <br> Fig 6: Boolean Expression for Carry output of a 1bit Full Adder. <br><br>
![image](https://github.com/user-attachments/assets/32b53627-752b-4a31-bc0d-cd08a8cf9c44) <br> Fig 7: Truth Table of a 1bit Full Adder. <br><br>
![1bit FA](https://github.com/user-attachments/assets/ebc14b51-ec7f-4dee-810e-93fde9df6390) <br> Fig 8: Schematic of a 1bit Full Adder. <br><br>

### 4bit RCA

![4bit RCA](https://github.com/user-attachments/assets/39caf6de-bcc7-4e6c-bb6f-5cc56478787f) <br> Fig 9: Schematic of a 4bit Ripple Carry Adder. <br><br>
![image](https://github.com/user-attachments/assets/adb79f83-cdc2-48c8-8c1c-60e61e14d465) <br> Fig 10: Waveform of a 4bit Ripple Carry Adder. <br><br>

## Layout
In this section, I will demonstrate how to construct the layout for a 4-bit Ripple Carry Adder (RCA). The process begins with creating the layouts for the individual components that make up the 4-bit RCA, specifically the Half Adders and Full Adders. Additionally, designing the layouts for the Half Adders and Full Adders necessitates constructing the layouts for the various logic gates involved in making of these adders. A maximum of two metal layers (metal 1 and metal 2) are used to form the connections (routes) for our design.

### Layout - Inverter (CMOS logic)
![Layout-inverter](https://github.com/user-attachments/assets/7ead02d4-ed05-4a24-9788-5d3cfe672c1d) <br> Fig 11: Layout of an Inverter. <br><br>

### Layout - AND Gate (CMOS logic)
![Layout-ANDgate](https://github.com/user-attachments/assets/2fc9de90-4040-4c39-87cf-9fdb96cf22e7) <br> Fig 12: Layout of an AND Gate. <br><br>

### Layout - XOR Gate (CMOS logic)

![Layout-XORgate](https://github.com/user-attachments/assets/40d20472-61ba-498d-8433-37a4d4257f69) <br> Fig 13: Layout of a XOR Gate. <br><br>

### Layout - OR Gate (CMOS logic)
![Layout-ORgate](https://github.com/user-attachments/assets/cccb0310-2348-4af7-aa7d-1a00f0628af3) <br> Fig 14: Layout of a OR Gate. <br><br>

### Layout - Half Adder (CMOS logic)
Since we know, to form a half adder requires a XOR and an AND gate. Similarly, we can can instantiate the layouts of these individual components to form the layout for a half adder. <br>
![Layout - Half Adder](https://github.com/user-attachments/assets/ea76913b-f6cb-4389-bd0d-d35e5e4855c6) <br> Fig 15: Layout of a Half Adder. <br><br>

### Layout - 1bit Full Adder (CMOS logic)
A 1bit full adder requires 2 half adders and an OR gate. We'll instantiate these already formed components to form a 1bit full Adder. Remember additional routing is to be done to connect these components of the FA :) <br>
![Layout-1bitFA](https://github.com/user-attachments/assets/3be72aea-2628-4983-8e88-c99df122132f) <br> Fig 15: Layout of a 1bit Full Adder. <br><br>

### Layout - 4bit RCA (CMOS logic)
A 4bit RCA requires four 1bit Full adders connnected in series (cascade fashion). We will instantiate them and connect the carry outs to carry in of the successive 1bit FA to form a 4bit RCA.
![Layout-4bitRCA](https://github.com/user-attachments/assets/a100aebe-2208-47e5-9dc6-3a28ed17d66e) <br> Fig 15: Layout of a 4bit RCA. <br><br>

## DRC and LVS checks
Our 4bit RCA layout is meets all the design rules specified for gpdk 180nm technology node and also meets the LVS requirements.

![Layout-4bitRCA-DRC](https://github.com/user-attachments/assets/17e797b2-a48b-40cc-b329-ecf62eaee01b) <br> Fig 16: DRC for 4bit RCA. <br><br>
![Layout-4bitRCA-LVS](https://github.com/user-attachments/assets/183ff7fb-b365-4d6f-831e-7caaa324d0aa) <br> Fig 17: LVS check (1/2) for 4bit RCA. <br><br>
![Layout-4bitRCA-LVS2](https://github.com/user-attachments/assets/8f23c51f-473f-4a68-81ef-f7db53b06d77) <br> Fig 17: LVS check (2/2) for 4bit RCA. <br><br>


**Note: All of these design or layout are performed in Cadence Virtuoso design tool. Cadence Assura tool is used for DRC and LVS checks for layout in gpdk 180nm library. Widths of PMOS is kept 2x the width of NMOS.**

























