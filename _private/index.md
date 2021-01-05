
# EE290C Spring 2021 <br/> Private Content 

Keeping this in the `_private` directory (or any directory beginning with `_`, `.`, and 
[a few other special characters](https://jekyllrb.com/docs/structure/)) 
will keep it from being published as part of the site. 

---

## Planning & To-Dos 

### Tues Dec 8, 2020

* Wrote initial, very rough, early part of schedule 
* [x] Invite Kris, Ali to this group 

### Tues Dec 15, 2020

Agenda: 

* Adding @aviral_pandey as GSI 
  * A key historian of this course, now having been involved with 3/4 iterations
  * First round taped out, next two didnt
  * Problems: ST digital tool-flow, analog effort-estimation (generally 2x off)
  * Digital integration, Liberty, LEF and similar collaterals, not well-understood at the time 
* BWRC sys-admin(s) on TSMC28
  * NDA includes export controls, in past students have voluntarily signed up for it 
  * Alternatives: Sky130, have non-NDA students do process-agnostic work e.g. Verilog
* Chip "Block Diagram"
  * Processor: primary goal is re-usability, research content e.g. min-config ChipYard/ Rocket
  * RF Transceiver: spring 2019 edition problems were largely LO freq tuning for BTLE range 
    * Will need to generate inductors, no existing p-cells in 28nm (likely none in 130 either), likely need existing BAG generator(s)
    * Existing 65nm BAG RF transceiver another potential source, mixer-first RX, power-noise trade-off 
    * Matching network & TX/RX switching: recommend off-chip 
  * Past RF Block List
    * Mixer 
    * LO 
    * PA 
    * Matching
    * RX Filter
    * RX VGA 
    * RX ADC 
    * I/Q would add DAC 
    * Supplies, regulation, bias, general analog stuff 
  * Baseband DSP, AXI/TileLink Interface 
    * Example from past here: https://github.com/ucberkeley-ee290c/fa18-ta
    * Expecting one student (Ryan Lund) will want (need?) to take this on 
    * Prior semesters should have Chisel for Hilbert filter, CDR, lots of related DSP 
  * Chip area, power, overall goals 
  * Top-level analog vs digital construction: past experience has been digital-top, hasn't gone great 
    * Roughly 200 analog-digital interface signals, one big analog block 
* ChipYard/ HAMMER Tutorial Run-Through (status: stuck) 
* Google Doc: https://docs.google.com/document/d/1uprSEXTuomGBG3UbTVRfO6_9R9SFg4fSLJiOHOk26mc/edit?usp=sharing_eip&ts=5fd872ef
* Past course designs/ tape-outs
   * Edward W tended to hide this, request access from him 

Action Items:

* [x] @bora working with BWRC staff on student NDAs/ access for TSMC28. ETA this week. 
* [x] @bora providing links to ADC & DAC generators he wants to use 
* [ ] @ali join https://github.com/ucberkeley-ee290c 
* [x] @bora setting up Piazza, will use for initial student backgrounds/ interests poll 
* [x] @dan will write up said poll

### Tues Dec 22, 2020

Agenda:

* TSMC28 Access
  * BWRC admins OK'ed student access 
  * MuseSemi OKed die area 
  * Need to define pad frame, area
  * Prior projects ~1x1 mm
  * Will be voluntary for students to sign TSMC28 NDA, needed near beginning of course 
  * Preference for HPM tech flavor
* SkyWater 130 SRAM
  * NDA-version PDK does have some (maybe one) SRAM 
  * Bora believes there's a compiler; haven't found it 
  * Arch recommendation: crank down SRAMs/ caches, likely to few kB, build from flops 
* Digital flow dry runs
  * ASAP-based runs going through with some help (Daniel G) 
  * Iterating on chip content, moving over to 28
  * No tape-outs in Hammer + TSMC28, yet 
* Blue Cheetah/ BAG3 Tutorial
  * BCA agreed to publish recent BAG3.1 tutorial by late Jan 
  * Unfortunately it's against an even-newer version of BAG than is public 
* BAG Methodology
  * Likely combination: BAG on bottom (base layers, matching placement, etc.), Virtuoso on top 
* Course Outline 
  * Needs git intro, BWRC compute early in course 
  * Digital FE - Verilog vs SV vs Chisel 
  * Analog - layout, matching
  * RF - Bora on baseband, Ali on everything else 

Action Items: 

* [ ] @bora - Students need TSMC28 NDA (very) early, before class starts, email them  
* [ ] @bora - Need to set early deadline for students to add this course, per NDA reqs. Typical deadline after first 3 weeks. 

### Tues Jan 5, 2021

Agenda:

* TSMC28 Access
  * BWRC Admins feedback - not OKed, still "just getting started" 
  * Received NDA from MuseSemi for TSMC28 HPC (high-perf compact), not HPM (high-perf mobile) 
  * Sending to students next week 
* Digital Flow Trials 
  * Slowly compiling matrix of tech (TSMC28/ Sky130/ ASAP), minimal configs 
  * Move these to `bora` queue, needs Unix group access 
  * Students will have separate queue and compute resource(s)
  * Jerry helping provide config stream-linings. Generally want something like SparkFun's RedBoard 
  * Nothing in chip-finishing, pad-ring, etc integrated with HAMMER/28 thus far 
* BAG(3) Status 
  * Basic layout generation works - inverter, delay line, etc. Few DRC rules to be cleaned up. 
  * Generated schematics don't work, maybe can work with twiddling Cadence CDF params 
  * ADC - Zhaokai shared https://bwrcrepo.eecs.berkeley.edu/zhaokai_liu/bag_vco_adc, which appears empty. Ping'ing him. 
* Reviewed Draft [Student Background/ Interests Poll](./poll.md)
* Initial Lecture/ Course Meeting Plans 
  * Bora doing first lecture - Intro, (hopefully) Rocket chip config 
* BWRC Admins (Brian R) agreed to do infrastructure & security training 

Action Items: 

* [ ] Lots of stuff setting up accounts
* [ ] @bora - set up dedicated compute machine/pool for students 

