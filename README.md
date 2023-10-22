# Final project FPGA: junk breaker (Sp22 Advanced Digital Lab)

## Team Members
Jun (Jerry) Yin, Xuanjia (Eric) Bi

Department of Electrical and Computer Engineering

University of Virginia

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

![image](https://github.com/AyaseErii/Junk_breaker/assets/70917894/07f775e1-5090-47c3-9f2a-6d72658ad3a2)

This project uses VGA (video designs cluster) as FPGA board display. VGA is an array of visual standard presented during the period of 1980s by IBM in their Personal Computers and is broadly upheld in illustrations equipment and screens. On the Hardware side, the VGA in this project as the traditional ones has Monitor, Color Information, and Adapter as following. 

### VGA Monitor:

A VGA Monitor acts as a grid of pixels -- 480 rows and each row consists of 640 pixels -- and each pixel is waiting for the color information that comes from the FPGA. 

### Color Information:
Colors is represented by the intensities of each fundamental color (Red, Green, Blue). The monitor expects these values to be analog; thus, a DAC (Digital to Analog Convertor) is used. The DE2 Educational Board has a 10-bit DAC, that is, it uses 10 bits to represent the intensity of each channel (Red, Green, or Blue), for a total of 30 bits. Depending on the type of monitor and video card you use at home, your computer uses either 16, 24, or 32 bits to encode this color information.

### VGA Adapter:

Since the VGA monitor does not have memory, the monitor will not store the pixel information being written to it. In order to achieve a stable image display, The VGA Adapter does have its own memory, and it will be responsible for constantly sending out the pixel information.

![image](https://github.com/AyaseErii/Junk_breaker/assets/70917894/aad15af6-96c7-4731-9dd4-1157b83fe4d7)

Above figure is the VGA cable pin configuration. Pin 1 to Pin 3 are the color information for the video. Pin 4, Pin 11, Pin 12, and Pin 15 are formerly used for Monitor ID through bit 0 to bit 3. Pin 5 and Pin 10 are the ground. Pin 6 to Pin 8 are the color return value. Pin 10 now connects to the +5V DC and powers EDID EEPROM chip. Pin 13 and Pin 14 are the horizontal synchronization and vertical synchronization also the clock data. 

### VGA Technical Specs:

* Selectable 25.175 MHz or 28.322 MHz master pixel clock
* Maximum of 640 horizontal pixels (graphics mode)
* Maximum of 480 lines
* Refresh rates at 60 or 70 Hz
* Packed-pixel mode: 256 colors
* Maximum 256KB of onboard display memory
 
This project uses 25.175 MHz Clock, 160 x 120 resolutions, and 8 color palettes for the simplicity of demonstration purpose.
* [Online Junk Breaker Game](https://poki.com/en/g/brick-breaker)
* [VGA basics](https://ieeexplore.ieee.org/document/8529621)

## Summary

By the end of the project, following progressions have been done to improve the Junk Breaker:

1. Most importantly, we have the playable game demo running smoothly in the FPGA Dec2-115 board

2. This game has colorful junk bricks for better UX 

3. Great amount of the junk bricks with meaningful junk brick arrangements 

4. Due to the right amount of the throughput design, this project does not have noticeable delay

5. Pause feature has been added on the board. 

6. Correct tuning on the travelling speeds of the ball and the paddle. 

7. Randomness, for example where the ball starts, was taken consideration to ensure unique experience as each time play 

![image](https://github.com/AyaseErii/Junk_breaker/assets/70917894/b7472ade-4826-4e5f-a37c-7f037f3865d0)

[Video link](https://drive.google.com/file/d/14iVcR7DsedkFIg9oaq4hHJ0VwIHtc9aL/view?usp=drivesdk) for the demo

Here are some future designs we planned to do if we had more time. 

1. Score Feature: the more junks have been eliminate, the higher score user will get

2. Different gaming level: there could have been different sets of difficulty for the game, such as more junks or take more than one hit to eliminate the junks

3. More randomness: the junks can appear in random positions

4. Dual paddles and dual balls feature designs for multiple players mode

## Presentation Slides

[Presentation](https://myuva-my.sharepoint.com/:p:/g/personal/htf6ry_virginia_edu/Efsad7DfrsRFvuSE-EHW3wUB2KcXeU-cF4-Y-fO0vR213g?e=3ALmFX)
