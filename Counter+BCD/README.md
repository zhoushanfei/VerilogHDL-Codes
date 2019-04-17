# Counter and BCD


**code requirements**


**A)**. Design the following circuit in Verilog and also write testbench. 
Make sure you use Task in your Verilog testbench.

![block diagram](https://github.com/mihir8181/VerilogHDL-Codes/blob/master/Counter%2BBCD/Block%20Diagram.png "Block Diagram")

Design a 4‐bit Up/Down counter that can count up, count down, or remain at the present value. 
The counter has four inputs RST, CLK, COUNT, and UPDN and one output VALUE. 
The ENABLE input is basically an enable signal that indicates when the counter should count. 
The UPDN input indicates which direction the counter should count. 
If ENABLE=1 and UPDN=1, the counter counts up incrementing VALUE on every clock cycle (e.g. 0, 1, 2, ...). 
If ENABLE=1 and UPDN=0, the counter counts down decrementing VALUE on every clock cycle (e.g. 5, 4, 3, ...). 
If COUNT=0, the counter does not count and instead retains the value presently held in VALUE.
The output of the counter is a 4‐bit value ranging from 0 to 15.

This value is the input to a second component that takes 4‐bit value and 
outputs the corresponding tens and ones values as a 4‐bit BCD encoding. 
For example if VALUE=4'b1110 (14), then TENS=4'b0001(1), ONES=4'b0100(4).


**B)** Write a Perl program to automatically create the testing input data and testing output data which you can use in your
Verilog testbench. Your Verilog testbench should compare the outputs values with the output data created by Perl program.

**Code Files**

Here in the Counter + BCD folder it includes the following files
[up_down_counter.v](https://github.com/mihir8181/VerilogHDL-Codes/blob/master/Counter%2BBCD/up_down_counter.v "up_down_counter.v") and 
its test bench [up_down_counter_fixture.v](https://github.com/mihir8181/VerilogHDL-Codes/blob/master/Counter%2BBCD/up_down_counter_fixture.v "up_down_counter_fixture.v")
[bin2bcd.v](https://github.com/mihir8181/VerilogHDL-Codes/blob/master/Counter%2BBCD/bin2bcd.v "bin2bcd.v") and 
its test bench file [bin2bcd_fixture.v](https://github.com/mihir8181/VerilogHDL-Codes/blob/master/Counter%2BBCD/bin2bcd_fixture.v "bin2bcd_fixture.v")
top fixture file is [updn_bcd_fixture.v](https://github.com/mihir8181/VerilogHDL-Codes/blob/master/Counter%2BBCD/updn_bcd_fixture.v "updn_bcd_fixture.v") which includes both module mentioned above.

Perl script [counter_bcd.pl](https://github.com/mihir8181/VerilogHDL-Codes/blob/master/Counter%2BBCD/counter_bcd.pl "counter_bcd.pl") to generate automated test vector for verilog.
data file [counter_bcd_datafile.txt](https://github.com/mihir8181/VerilogHDL-Codes/blob/master/Counter%2BBCD/counter_bcd_datafile.txt "counter_bcd_datafile.txt") which is generated by perl script, 
which consists of test vectors to test in verilog testbench.

![Log1](https://github.com/mihir8181/VerilogHDL-Codes/blob/master/Counter%2BBCD/Result_log%201.png "simulation log1")
![Log2](https://github.com/mihir8181/VerilogHDL-Codes/blob/master/Counter%2BBCD/Result_log%202.png "simulation log2")