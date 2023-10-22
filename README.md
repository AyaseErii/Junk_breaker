# Final project junk breaker (Sp22 Advanced Digital Lab)

## Objectives

1. Develop a game in Field-programmable gate arrays (FPGAs)
2. Familiarize with Hardware Description Languages (HDL) such as Verilog and VHDL
3. Troubleshoot on clock, ports, and software issue
4. Optimize performance and energy consumption
5. Improve gaming experience 
6. Minimize the task complexity for tutorial purpose

## Background

Junk Breaker (also called as Brick Breaker) is a Breakout clone which the player must smash a wall of bricks by deflecting a bouncing ball with a paddle. The paddle may move horizontally and is controlled with the BlackBerry's trackwheel, the computer's mouse or the touch of a finger (in the case of touchscreen). The player gets 3 lives to start with; a life is lost if the ball hits the bottom of the screen. When all the bricks have been destroyed, the player advances to a new, harder level. Many levels have unbreakable silver bricks. If all lives are lost, the game is over. 
This project will modify the original Junk Breaker to deliver a better gaming experience. 

[[File:Junk breaker.png|560 px|center]]

This project uses VGA (video designs cluster) as FPGA board display. VGA is an array of visual standard presented during the period of 1980s by IBM in their Personal Computers and is broadly upheld in illustrations equipment and screens. On the Hardware side, the VGA in this project as the traditional ones has Monitor, Color Information, and Adapter as following. 

### VGA Monitor:

A VGA Monitor acts as a grid of pixels -- 480 rows and each row consists of 640 pixels -- and each pixel is waiting for the color information that comes from the FPGA. 

### Color Information:
Colors is represented by the intensities of each fundamental color (Red, Green, Blue). The monitor expects these values to be analog; thus, a DAC (Digital to Analog Convertor) is used. The DE2 Educational Board has a 10-bit DAC, that is, it uses 10 bits to represent the intensity of each channel (Red, Green, or Blue), for a total of 30 bits. Depending on the type of monitor and video card you use at home, your computer uses either 16, 24, or 32 bits to encode this color information.

### VGA Adapter:
Since the VGA monitor does not have memory, the monitor will not store the pixel information being written to it. In order to achieve a stable image display, The VGA Adapter does have its own memory, and it will be responsible for constantly sending out the pixel information.

[[File:VGA pins conf.jpg|560 px|center]]
