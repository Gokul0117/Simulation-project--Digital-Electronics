### GRAY TO BINARY CONVERTION USING VERLOG

### AIM:
Design and simulate gray to binary converter using Verilog.

# THEORY
Gray codes are used in rotary and optical encoders, Karnaugh maps, and error detection. The hamming distance of two neighbours Gray codes is always 1 and also first Gray code and last Gray code also has Hamming distance is always 1, so it is also called Cyclic codes. You can convert a Gray code to Binary number using two methods.

Using Karnaugh (K) - map −

You can construct Gray codes using other methods but they may not be performed in parallel like given above method.

This is very simple method to get Binary number from Gray code. These are following steps for n-bit binary numbers −

Using Exclusive-Or (⊕) operation −

This is very simple method to get Binary number from Gray code. These are following steps for n-bit binary numbers −

1.The Most Significant Bit (MSB) of the binary code is always equal to the MSB of the given binary number. 2.Other bits of the output binary code can be obtained by checking gray code bit at that index. If current gray code bit is 0, then copy previous binary code bit, else copy invert of previous binary code bit.

For example, for 3-bit binary number, let Binary digits are b2 , b1 , b0, where b2 is the most significant bit (MSB) and b0 is the least significant bit (LSB) of Binary. Gray code digits are g2 , g1 , g0, where g2 is the most significant bit (MSB) and g0 is the least significant bit (LSB) of Gray code.

# LOGIC DIAGRAM
### Procedure:
```
Developed by : Gokul j
Reg no : 212222230038
```

### Program:
```
module graytobinary(
input [5:0] gray,
output [5:0] binary
);
assign binary[5] = gray[5];
assign binary[4] = gray[5] ^ gray[4];
assign binary[3] = gray[4] ^ gray[3];
assign binary[2] = gray[3] ^ gray[2];
assign binary[1] = gray[2] ^ gray[1];
assign binary[0] = gray[1] ^ gray[0];
endmodule


```
### Logic Diagram:
![Screenshot 2023-06-17 110502](https://github.com/Gokul0117/Simulation-project--Digital-Electronics/assets/121165938/78fb9be3-e7ca-474c-8202-e30dedb07265)


# NETLIST DIAGRAM
![Screenshot 2023-06-17 105656](https://github.com/Gokul0117/Simulation-project--Digital-Electronics/assets/121165938/36da494a-f79c-4f86-a06b-b086a9940d8b)


# TIMING DIAGRAM:
![WhatsApp Image 2023-06-17 at 11 15 29](https://github.com/Gokul0117/Simulation-project--Digital-Electronics/assets/121165938/9d290acd-7590-49cd-a34f-45fb56369452)


# REFERENCE
Gokul0117
/
Simulation-project--Digital-Electronics
