# Advanced Topics in Circuit Design 
## 28nm SoC for IoT 

In this class, we will design and send out for fabrication a
system-on-a-chip (SoC) intended for internet-of-things applications
(IoT).  The chip will contain a RISC-V microprocessor, a radio
transceiver, and a baseband signal processor, and will be designed in
a 28nm CMOS process (And we really mean it!)

The course will be hands-on, covering many of the aspects of practical
integrated circuit design, using state-of-the art tools in a modern
technology. The students should expect to start practical design
through guided laboratory exercises from the very beginning, and all
students interested in this exciting opportunity will need to sign up
by the end of the first week of classes.

--- 

## Topics 

* Our SoC for IoT
    * State-of-the art micro-robotics, RISC-V, low-power RF 
* Digital Front-End Design 
    * Verilog, Chisel
* Digital Back-End 
    * Logic Synthesis, Place-and-Route Layout, HAMMER, Clock & Power Networks 
* Analog Design Practice
    * Design for layout, matching, performance 
    * Cadence, ADE, OCEAN, SKILL, Extraction
* Analog Generators 
    * BAG Framework, Python
* Chip & Tape-Out Practice
    * ESD, IOs, Package & PCB Design 
* RF, Wireless, Signal Processing 


## Lecture Schedule 

| Week(s) | Date(s)     | Agenda                                      |                |
| ------- | ----------- | ------------------------------------------- | -------------- |
| 1       | 1/19        | Course Intro, Our Chip | [Slides](https://drive.google.com/file/d/1FV78X3iNcFyxaLOvjwVR6R8wI_zvcF8G/view?usp=sharing) |
|         | 1/21        | BWRC Orientation | [Slides](https://drive.google.com/file/d/1QIy9ShYp3JyN0DxwnQvG-xXvsr9WZu07/view?usp=sharing) |
| 2       | 1/26-1/28   | Team Formation <br> ChipYard Intro | [Slides](https://drive.google.com/file/d/1HnRFrYKzJU2kpmtHaocyfN1TqhUVv2Te/view?usp=sharing) |
| 3       | 2/2         | RF Systems Overview                         |               |
| 3-4     | 2/4-2/11    | Hierarchical Design Flow                    | [Notes](./notes) |
| 5-6     | 2/16-2/23   | Analog & RF Layout                          |               |


## Design Schedule 

| Week(s)     | Date(s)     | Design Calendar                           | Academic Calendar |
| ----------- | ----------- | ----------------------------------------- | -------------- |
| 1           | 1/19-1/21   | Intro To Our Chip                         |                |
| 2           | 1/28        | Initial Presentations                     |                |
| 3           | 2/4         |                                           |                |
| 4           | 2/11        |                                           |                |
| 5           | 2/18        |                                           |                |
| 6           | 2/25        | Prelim Interfaces, Specs, and Floor-Plans |                |
| 7           | 3/4         |                                           |                |
| 8           | 3/11        | Prelim Schematics & RTL <br/> Trial Integration, Interface Lock |                |
| 9           | 3/18        | Industry-Partners Design Review           |                |
| 10          | 3/25        | -                                         | *Spring Break* |
| 11          | 4/1         | Mock Tape-Out                             |                |
| 12          | 4/8         | RTL & Schematic Freeze                    |                |
| 13          | 4/15        |                                           |                |
| 14          | 4/21        | Final Sub-Block Layout                    |                |
| 15          | 4/28        | Full-Chip LVS & DRC Clean Layout          |                |
| 16          | 5/5         | Foundry Feedback <br/>Final Layout        | *Reading Week* |
| 16          | 5/12        |                                           | *Exam Week*    |
| ...         |             |                                           |                |
|             | 7/29        | Wafers Ship Back to Berkeley              |                |


## Staff

* Faculty 
    * Borivoje Nikolic bora@berkeley.edu
    * Kris Pister ksjp@berkeley.edu
    * Ali Niknejad niknejad@berkeley.edu
* GSIs
    * Dan Fritchman dan_fritchman@berkeley.edu
    * Aviral Pandey aviral0607@berkeley.edu

## Lectures and Office Hours

|               |                                                                |
| ------------- | -------------------------------------------------------------- |
| Lectures      | Tues, Thurs	3:30 - 5 pm	                                       |
| Office Hours  | Thurs	11:00 am - 12:00 pm	   Dan Fritchman                    |
|               | Thurs 12:00 am - 1:00 pm		Avi Pandey                       |


## Links 

* [*Tapeout class: Taking students from schematic to silicon in one semester*](https://ieeexplore-ieee-org.libproxy.berkeley.edu/stamp/stamp.jsp?tp=&arnumber=8351506) David C. Burnett; Brian Kilberg; Rachel Zoll; Osama Khan; Kristofer S. J. Pister, 2018 IEEE International Symposium on Circuits and Systems (ISCAS)
* ChipYard [Repository](https://github.com/ucb-bar/chipyard) and [Documentation](https://chipyard.readthedocs.io/en/latest/)
* Chisel [Bootcamp](https://github.com/freechipsproject/chisel-bootcamp)
* [Course Archives](https://inst.eecs.berkeley.edu/~ee290c/archives.html)
* [Piazza Forum](https://piazza.com/class/kiqf7tz0bsp1oj)
* [bCourses Site](https://bcourses.berkeley.edu/courses/1500979)
* [GradeScope](https://www.gradescope.com/courses/214436)

