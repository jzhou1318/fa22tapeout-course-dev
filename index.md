# Advanced Topics in Circuit Design
## 22nm SoC for IoT

In this class, we will design and send out for fabrication a
system-on-a-chip (SoC).

<!-- TODO: Blurb on what the chip is -->
<!-- The chip will contain a RISC-V microprocessor, a radio -->
<!-- transceiver, and a baseband signal processor, and will be designed in -->
<!-- a 28nm CMOS process (And we really mean it!) -->

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
| 1       | 1/19        | Course Intro, Our Chip                      |[slides](https://docs.google.com/presentation/d/1O6NQxIgmDE3Ufo8fASbfssEy0wwD0lQ2/edit?usp=sharing&ouid=114241049124280929588&rtpof=true&sd=true) [Recording](https://drive.google.com/file/d/1W4mxO4KyndbOJxWArM4YXtXkEMy6Uxjw/view) |
|        |         |                       |[SCUM-V Intro](https://docs.google.com/presentation/d/11S1dx3a6r4vA29wQQcYUO5wl2g7PSl9p/edit?usp=sharing&ouid=114241049124280929588&rtpof=true&sd=true)  |
|        |         |                       |[Chipyard Lab](./chipyardlab)  |

<!-- |         | 1/21        | BWRC Orientation                    | [Slides](https://drive.google.com/file/d/1QIy9ShYp3JyN0DxwnQvG-xXvsr9WZu07/view?usp=sharing) | -->
<!-- | 2       | 1/26-1/28   | Team Formation <br> ChipYard Intro  | [Slides](https://drive.google.com/file/d/1HnRFrYKzJU2kpmtHaocyfN1TqhUVv2Te/view?usp=sharing) | -->
<!-- | 3       | 2/2         | RF Systems Overview                         |               | -->
<!-- | 3-4     | 2/4-2/11    | Hierarchical Design Flow            | [Notes](./notes) | -->
<!-- | 5-7     | 2/16-3/4    | Analog & RF Layout                          |               | -->
<!-- | 8       | 3/9         | Design Updates                              |               | -->
<!-- |         | 3/11        | Guest Lecture: Testing & Bring-Up   | [Slides](./assets/ee290_bringup_guest_lecture.pdf) | -->
<!-- | 9       | 3/16-3/18   | Industry Design Review              | [Slides](./assets/review-mid.pdf) | -->
<!-- | 10      | 3/23-3/25   | *Spring Break*                              |               | -->
<!-- | 11      | 3/30        | Design Updates                              |               | -->
<!-- |         | 4/1         | Guest Lecture: Package & PCB Design | [Slides](https://drive.google.com/file/d/1LKhzhb_q6fVETYbvka6vH6LdFAwouZzB/view?usp=sharing) | -->
<!-- | 12      | 4/6         | Guest Lecture: Mixed-Signal Verification    |               | -->
<!-- | 12-16   | 4/8-5/6     | Design Updates                              |               | -->
<!-- |         | 5/17        | Industry Design Review              | [Slides](./assets/review-final.pdf) | -->


## [Design Schedule](./milestones)

TBD

<!-- | Week(s)     | Date (Thurs) | Design Calendar                          | Academic Calendar | -->
<!-- | ----------- | ----------- | ----------------------------------------- | -------------- | -->
<!-- | 1           | 1/21        | Intro To Our Chip                         |                | -->
<!-- | 2           | 1/28        | Initial Presentations                     |                | -->
<!-- | 3           | 2/4         |                                           |                | -->
<!-- | 4           | 2/11        |                                           |                | -->
<!-- | 5           | 2/18        |                                           |                | -->
<!-- | 6           | 2/25        | Prelim Interfaces, Specs, and Floor-Plans |                | -->
<!-- | 7           | 3/4         |                                           |                | -->
<!-- | 8           | 3/11        | Prelim Schematics & RTL <br/> Trial Integration, Interface Lock |                | -->
<!-- | 9           | 3/18        | Industry-Partners Design Review           |                | -->
<!-- | 10          | 3/25        | -                                         | *Spring Break* | -->
<!-- | 11          | 4/1         | Mock Tape-Out                             |                | -->
<!-- | 12          | 4/8         | RTL & Schematic Freeze                    |                | -->
<!-- | 13          | 4/15        |                                           |                | -->
<!-- | 14          | 4/21        | Final Sub-Block Layout                    |                | -->
<!-- | 15          | 4/28        | Full-Chip LVS & DRC Clean Layout          |                | -->
<!-- | 16          | 5/5         | Foundry Feedback <br/>Final Layout        | *Reading Week* | -->
<!-- | 16          | 5/12        |                                           | *Exam Week*    | -->
<!-- | ...         |             |                                           |                | -->
<!-- |             | 7/29        | Wafers Ship Back to Berkeley              |                | -->


## Staff

* Faculty
    * Borivoje Nikolic [bora@berkeley.edu](bora@berkeley.edu)
    * Kris Pister [ksjp@berkeley.edu](ksjp@berkeley.edu)
    * Ali Niknejad [niknejad@berkeley.edu](niknejad@berkeley.edu)
* GSIs
    * Sherwin Afshar [sherwina210@berkeley.edu](sherwina210@berkeley.edu)
    * Paul Kwon [hyunjaekwon@berkeley.edu](hyunjaekwon@berkeley.edu)
	* Zhaokai Liu [zhaokai\_liu@berkeley.edu](zhaokai_liu@berkeley.edu)
    * Jerry Zhao [jzh@berkeley.edu](jzh@berkeley.edu)
    * Bob Zhou [bob.linchuan@berkeley.edu](bob.linchuan@berkeley.edu)


## Lectures and Office Hours


|               |                                                                |
| ------------- | -------------------------------------------------------------- |
| Lectures      | Monday, Wednesday	2:00 - 3:30 pm	                         |
| Office Hours  | Bora: Thursdays 11am - 12pm (See Piazza for Zoom Link)         |



## Links

* [Piazza](https://piazza.com/class/kyer4edhzkd5wy?cid=10)
* [Slack](tapeout.slack.com)
<!--  * [BWRC Repos](https://bwrcrepo.eecs.berkeley.edu/ee290c_ee194_intech22) -->

<!-- * [*Tapeout class: Taking students from schematic to silicon in one semester*](https://ieeexplore-ieee-org.libproxy.berkeley.edu/stamp/stamp.jsp?tp=&arnumber=8351506) David C. Burnett; Brian Kilberg; Rachel Zoll; Osama Khan; Kristofer S. J. Pister, 2018 IEEE International Symposium on Circuits and Systems (ISCAS) -->
<!-- * ChipYard [Repository](https://github.com/ucb-bar/chipyard) and [Documentation](https://chipyard.readthedocs.io/en/latest/) -->
<!-- * Chisel [Bootcamp](https://github.com/freechipsproject/chisel-bootcamp) -->
<!-- * [Course Archives](https://inst.eecs.berkeley.edu/~ee290c/archives.html) -->
<!-- * [Piazza Forum](https://piazza.com/class/kiqf7tz0bsp1oj) -->
<!-- q* [bCourses Site](https://bcourses.berkeley.edu/courses/1500979) -->
<!-- * [GradeScope](https://www.gradescope.com/courses/214436) -->
