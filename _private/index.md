
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

* [x] @bora - Students need TSMC28 NDA (very) early, before class starts, email them  
* [x] @bora - Need to set early deadline for students to add this course, per NDA reqs. Typical deadline after first 3 weeks. 

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

* [x] Lots of stuff setting up accounts

### Tues Jan 12, 2021

Agenda:

* Student Communications Status 
  * Interests poll up on Piazza, one response so far 
  * Kris added all students to Piazza
  * No dept solicitation email (yet) 
  * Currently 22 students between 290C/194 
* TSMC28 Access Status 
  * MuseSemi can offer TSMC28 HPC variant 
  * BWRC Admin says we dont have HPC content
  * Need to send NDA via email for students to (voluntarily) agree to (or not)
  * @bora drafted one of these emails, waiting for (some?) confirmation to send 
  * Plan for MuseSemi 1x1
    * Prior versions 1.1x1.1 total, ~0.9x0.9 circuit, rest pads 
* Meeting on ChipYard-based lab sharing last Friday
  * Covered us, dig-course, arch-course, HW-ML-course
  * We are largely paired with the digital course in (if we have labs) doing: 
    * Run Chisel -> Verilog in ChipYard 
    * Push Verilog through PnR via HAMMER 
  * ChipYard Lab - https://www.overleaf.com/project/5ff89d07f3c28f15fffb5ecb
  * @avi plans to construct analog/layout lab
* Digital Flow Trials 
  * TSMC28 HAMMER trials now including inline-generated SRAMs 
  * Group w/ Jan Rabaey also editing HAMMER plug-in 
  * Arya R-P rolling in HAMMER plug-in updates 
  * HAMMER plug-in: https://bwrcrepo.eecs.berkeley.edu/tstech28/hammer-tstech28-plugin
* BWRC Admin Training in Lecture #2, Thurs 1/21

Action Items: 

* [x] @kris - consult with @bora re sending department solicitation email. Send by this Friday, or don't.
* [x] @kris / @bora - students need BWRC accounts by Thurs 1/21 ("drop dead date")
* [x] @bora - TSMC NDA email 
* [x] @dan will share editing of CY labs
* [x] @avi - design of initial layout lab 
* [x] @bora - set up dedicated compute machine/pool for students 


### Tues Jan 12, 2021 (Doubleheader) 

Agenda:

* Dept solicitation email went out 
* TSMC28 update - got new NDA, no EAR requirement. Should be distributable soon. 
  * We need to get the 28 HPC content - pending NDA signature, hopefully download tomorrow morning 
* RF Baseband
  * Have past RTL, old version of Chisel 
  * Student Ryan Lund dusting it off, likely ~ 7wk or more 
  * Was hooked up to ARM, different CPU interface 
  * Could alternately feed ADC data direct to CPU 
* Lecture 1 plan - chip & course overview, Bora planning to lecture 
  * Chip design & tape-out process
  * Content of our chip
  * Tools of each section, what we plan to use
  * Prospective timeline 
* Reading 
  * Kundert top-down paper, primarily for analog - https://designers-guide.org/design/tdd-principles.pdf

Action Items: 

* [x] @dan adding poll on whether students have EECS, BWRC accounts


### Tues Jan 19, 2021 

Agenda:

* First Lecture Today 
  * Slides in https://drive.google.com/drive/folders/1unDbLAbhtphpWxSWN-cnuJ1SP-AEI48F?usp=sharing_eip&ts=600545df
  * @dan added several this morning 
  * @bora posting Zoom link for lecture 
* Student Background/ Interests Compilation 
  * At https://docs.google.com/spreadsheets/d/1hplb9Z_7FnNUo0PhU-6-kT6RhHMyovPSAs2sZPMetd8/edit?usp=sharing
  * As of yesterday 1/18:
    * 12/22 students responded
    * About 2/3 respondees interests are digital 
    * About half those have no analog background whatsoever
    * RF looks especially thin 
* Prospective Chip Block Diagrams
  * Figures at https://drive.google.com/file/d/1A-jCj9OLzbHNaBEwbqSbI-o4KXXHci5P/view?usp=sharing
  * Discussed - pull out peripheral RF (matching, combining, PLL, etc), add accelerators for ML/ crypto 

* Infrastructure Setup
  * Poll on BWRC accounts - 4 students have accounts, remaining 18  don't
  * Students were emailed, asked to send in BWRC app to Candy. As of last night she had received 9. 
  * No group/batch enrollment, remaining students will need to submit form
  * @bora announcing students who haven't requested by Friday will be dropped  
  * @dan adding email announcement to Piazza
  * @brianr presenting on Thursday, BWRC security & practices 
  * Git practices also to be covered Thursday, @dan / @avi will sort this out 
* Tech Access Status 
  * TSMC NDA email to students coming today
  * TSMC28 HPC files not on-hand 
  * @brianr OK granting access to HPM in interim 
  * General agreement with BWRC, Muse, TSMC in place 

* Upcoming Lecture Plans/Schedule 
  * @bora on ChipYard Thurs 
  * Plan to have short lecture + student presentations after week 2-3 
  * Simone Gambini guest lecture on BTLE 
* Grad vs U-Grad Course Diff 
  * Prefer to have codified difference in expectations 
  * Announce leadership expectations
  * Potential venues: tougher blocks, block leadership, specs & docs, write-up
  * @bora planning to write up specs/docs responsibility 
* Related Course Co-Projects
  * @bora offering to 241 students
  * @ali planning to make similar offer to ana/RF students 

Didn't Get To:

* Office Hours?
* What's everybody do until they get tech access? 

Action Items:

* [x] @bora distributing lecture Zoom link
* [x] @bora distributing NDAs today 
* [x] @dan adding Piazza post on account setup 
* [x] @dan / @avi sorting out Thurs git presentation 


### Tues Jan 26, 2021

Agenda:

* Tues lecture - @bora on ChipYard, @dan / @avi on block diagram & assignments 
* Thurs lecture - discussed RF overview, no slides but hand-drawn 
  * @kris on RF system overview - 50min
  * Initial student presentations Thurs - 5min each, 25min total
* Next Tues - @dan on hierarchical big-chip design flow 
* TSMC/ NDAs in progress, hopefully next few days 

Action Items: 

* [x] @bora today's slides
* [x] @dan, @avi block assignment section of today's lecture


### Fri Jan 29, 2021

Agenda:

* NDA status, TSMC28 HPM vs HPC setups
  * HPC PDK downloaded, @brian working through unpacking, "first pass" complete 
  * Looks like students (all?) are in `tstech28` group, enabling HPM-based labs
* Follow-up on block diagram, student decisions 
  * Generally like the plan, continue to provide input and detail 
* Next week lecture plans 
  * Tues @kris on RF systems 
  * Thurs @dan on top-down/ industrial-grade flow stuff 
  * Thurs have half the groups - compute & accelerators - present 15min each 

Action Items: 

* [ ] @bora choose a reading on layout 
* [ ] @avi digging up past CORDIC lab 
* [x] @kris Tues lecture/ talk (50min) 
* [x] @dan next Thurs lecture/ talk 


### Fri Feb 5, 2021

Agenda: 

* Follow-up on student presentations/ progress
  * Proposal - 64kB iMem, 64kB dMem, no layered hierarchy 
  * Proposal - no RTOS, bare-metal POR 
  * @kris believes RTOS should only need 5-10kB, if we even want one 
  * @bora looking at 64b Zephyr, fits in 32kB, checking whether fits smaller 
  * @dan will send them the SiFive datasheet, maybe a few smaller ones 
  * @ali will write up proposed RF transceiver specs
* Labs
  * 8 students submitted ChipYard (posted due Thurs)
  * 4 submitted analog (due tonight)
* 28HPC Status  
  * PnR stuck on QRC tech file
  * SRAM compiler should have been added today 
  
Didn't Get To: 

* Next week's lecture schedule 
* Follow-up past AIs
* Revisit design schedule 

Action Items: 

* [x] @bora sending datasheets 
* [x] @ali sending proposed RF specs (students did well to make these!) 


### Fri Feb 12, 2021

Agenda: 

* Upcoming Week's Lectures/ Meetings
  * Announced student presentations every lecture unless we announce otherwise 
  * Upcoming: @ali on layout Tues & Thurs 
  * Future Topics:
    * @ali (or delegate) - ESD & latch-up
    * @avi - BAG/ associated design process 
    * @avi - Verilog-A for simulation & test-benching 
    * @ali (possibly) OCEAN/ SKILL/ other Cadence-scripting
    * More on timing analysis, debugging thereof 
    * Testing / bring-up / lab intro. Packaging, off-chip interfaces, PCB, equipment etc. 
* 28HPC Setup Status 
  * Got correct QRC file(s) from Muse/TSMC, PnR and SRAM up and running 
  * Updates to ChipYard lab posted as demo for students, some appear to be trial'ing
  * No BAG yet, should be relatively straightforward port from 28HPM
* Follow-up on student presentations/ progress
  * Compute - memory-mapping, peripherals. Calling in @abe on this. 
  * RF - working on setting up deep(er) dive with @ali 
    * Re-arranging a bit, move one of the filter-designers to LO 
  * Integration - area distributions, physical-design partitioning 
* ADC Generator
  * Zhaokai reporting some porting-trouble, @avi reaching out 
  * Also then needs the HPM->HPC port 
  
Action Items: 

* [x] @dan & @avi setting up session with integration team 


### Fri Feb 19, 2021

Agenda: 

* Upcoming Week's Lectures/ Meetings
  * @ali layout ongoing, will continue through Tues
  * @avi Thurs - Verilog-A, BAG if time permits 
  * Following Tues, try to line up BAG ADC generator w/ Zhaokai 
  * @ali (or delegate) - ESD & latch-up
  * @bora could do baseband in ~ 2wk
* Design Status 
  * BAG bring-up remains ongoing, @avi working with Zhaokai on ADC generator 
  * CPU/ Mem-system meeting with Abe Thurs, generally pushed back towards cache. 
    * Cheng seems to be doing everything. Nayiri probably overloaded, not clear what Josh is doing. 
  * Accel - plan looking good, primary remaining question is interaction with memory system. 
    * Anson seems to be doing everything. Unclear what Eric & Daniel doing 
  * Radio BB - seem to have good handle, making progress
  * RF PLL - DCO design proceeding with Alex, Sherwin going slower, way less background on FLL/PLL 
  * Radio front-end - @avi conveying lack of expectation they'll get Sashank RX 
  * Analog baseband - appears to be all Jeffrey, haven't heard from others (Kerry, Leon)
  * Integration/ Verification - met with TAs Tues, got them started on block diagram, floor-plan, chip IOs 
  * LDOs getting started, no news on clocking 
  * @avi putting together draft pad-ring 
* Teams Sheet reminder: https://docs.google.com/spreadsheets/d/1hplb9Z_7FnNUo0PhU-6-kT6RhHMyovPSAs2sZPMetd8/edit#gid=0

Action Items 

* [ ] @avi line up Zhaokai for BAG/ADC presentation 
* [x] @avi setting up Virtuoso layout session, outside lecture 
* [x] @dan reaching out to Daniel re bring-up 


### Fri Feb 26, 2021

Agenda: 

* Upcoming Lectures
  * @ali finish layout Tues
  * @avi analog testing, Verilog-A, etc Thurs
  * Daniel G to follow on bring-up 
  * Zhaokai to follow that(?) 
  * Simone Guest lecture - first week of April 
  * SV Test-benching, assertions
* Chip Bring-Up
  * Daniel G described existing bring-up setup, and it's pretty elaborate
  * FPGA running Linux soft-core, with its own (custom?) Linux, talking OpenOCD over JTAG to the DUT
  * Simpler commercial setup: https://github.com/sparkfun/Red_V 
  * Asking Daniel G to guest-lecture on this setup, @dan will prepare some content on simpler setups 
* ChipYard - merging v1.4 into their lab-version
  * Config used for lab was removed, as were most "SmallRocket" configs
* Design Schedule
  * Updated https://ucberkeley-ee290c.github.io/sp21/
  * @bora & @ali presenting their admonishments to follow it on Tues
  * @dan writing up some more detail on these milestones
* ADC - Zhaokai working on porting, should be reaching out to @avi 
* Design Status 
  * CPU 
    * Been tough to extract any design-work from them. 
    * Seeing DRC attempts was progress. 
    * Still not much sign of Josh A. 
    * Still no idea how or whether this thing will ever boot. 
  * Accel 
    * Probably furthest along 
    * Found some reference software; may require some help getting anything running. 
    * Added a 2nd visible contributor, still not much sign of the 3rd
  * LDOs/ Jackson 
    * Hadn't done anything as of Weds. Now at least trying stuff. Propose letting him proceed. 
  * SoC PLL/ Kareem 
    * Hadn't done anything as of Weds. Still doesn't appear to have done anything. Meeting on Monday, probably gotta cut him off if he's not producing anything. Question is what to move him to. 
  * Top-Level / Integration 
    * Meeting with them regularly, slowly getting moving. Dylan picking it up, Troy less so. 
  * Radio 
    * RX Front-End - Felicia working on mixer-first, showing progress 
    * TX - not much progress, looking to Shreesha for this
    * Analog Baseband - not much progress, @avi meeting with them
    * LO - Alex has shown some work, needs adding control/ tuning 
    * LO PLL - Sherwin in early days, looking at CppSim, referred him to some MATLAB models 
    * Digital Baseband - doing great on design internals. Starting to talk with other teams about actually getting CPU, BB, and RF PHY to talk. 
    * (Other sub-systems) - TBC 


Action Items 

* [ ] @bora starting deck on SV/ digital test tactics, assertions et al 
* [x] @dan starting deck on embedded bring-up environments - https://ucberkeley-ee290c.github.io/sp21/notes


### Fri March 5, 2021

Agenda: 

* Upcoming Lectures
  * Tues - @avi analog testing, Verilog-A, etc 
  * Thurs - Daniel G to follow on bring-up 
  * Tues 3/16 - all-student time, prep for design review
  * Thurs 3/18 - design review. Meeting w/ Ramesh next week. 
  * Week after that - Spring Break 
  * After break - James Dunn on packaging & friends
* ADC Status
  * @avi running through BAG TSMC28HP**M**
  * Missing input sampling
  * Rest seems to look OK
  * Still needs converting to HPC 
* Design Review Plan 
  * Plan to extend this to 2.5hr - check with students 
  * How long is Apple team OK to participate? 
  * Meeting w/ Ramesh next Tues, should offer some detail 
  * What is OK to share: everything but "raw PDK data". "Derived" are OK. 
* Design Status 
  * Dropped SoC/CPU PLL, re-directed Kareem to help Sherwin on LO PLL
  * Anson complaining accelerator teammates not doing anything, especially Daniel. Eric doing some SW now. 
  * @bora asked Daniel to write Verilog TB for AES SV IP. No real contribution so far. 
  * Also caught up with Ryan, thinks he needs to write all the Chisel, Griffin not familiar with it, doing Chisel bootcamp 
  * Challenged CPU to produce sim of boot process 
  * RF 
    * Felicia going OK on RX front-end
    * Alex seems stuck on DCO 
    * Sherwin largely driving LO PLL, now has Kareem help 
    * Baseband showed some stuff, better than not seeing anything 
    * Spec division down to sub-blocks hasn't really seemed to happen. Make Felicia the owner of this. 
    * Missing in action: Shreesha, Leon Wu 
  * Plan to get Jackson in on RF top-level, especially for layout phase 

Action Items 

* [ ] @ali meeting with Felicia on RF budgeting 


### Fri March 12, 2021

Agenda: 

* Design Review Planning 
  * Apple "source" claims 10 accepted for Tues, 6 for Thurs
  * "CPU, AMS, a bit of RF, verification, digital circuits" backgrounds
  * Run til 6pm Tues, maybe a bit beyond 5pm Thurs 
  * Will post link to starter Google-slides
  * Require slides by Monday 5pm 
* Distribution of Time 
  * Kris - history, past course iterations, updates for this year
  * Bora - prior research infrastructure (CY, Chisel, BAG ADC, etc) 
  * Chip Overview: 15min - Anson, Ryan, Nayiri, Felicia 
    * Chip block diagram, spec targets, teams 
  * Tues 2.5hr: up to 30min each
    * CPU, AES Accel, RF BB, Integration 
  * Thurs 1.5hr - tell everybody to be ready Tues, but plan for: 
    * RF Transceiver 1hr, other analog 30min
* Student Reminders:
  * Intros, photos, one-line student bios 
  * Recommend turning on video to present! 
  * External reviewers won't know any Berkeley-specific stuff (Rocket, Hammer, Chisel tools, etc) 
  * Stuff that is industry-general: analog, Virtuoso, Verilog, synth/PnR tools 

* Design Status 
  * AES - gotta start simulating SV core, nothing on that yet 
  * LO VCO seems to have stalled, hopefully got message to get rolling 
  * Analog BB ramping up after a slow start 
  * Analog layout - about where 1st course was
  * Gotta get some trial layout before schematic freeze 
  * Kareem working on IO/pad ring, sifting through IO cells, @avi following up 
  * Package - planning for 40-pin QFN 

Action Items 

* [ ] All - "pound on" spec, add comments, try to generate students agreeing on sections 
* [x] @avi - announcing need for trial layout before 
* [x] @avi following up on RF floor-plan 
* [ ] @avi checking with Quik-Pak on package/bond-wire OK-ness 
* [x] @dan announcing all this other design review stuff 


### Fri March 19, 2021

Agenda: 

* Next week Spring break 
* Week After 
  * Tuesday - Avi
  * Thursday - James 
  * Following Tues - Simone 
  * Following Thurs - Bora on radio baseband 
* Design Review Follow-Up 
  * A Few Themes of Feedback 
    * In-Circuit Testability & Debuggability
    * Verification 
    * Attention on Analog-Digital Crossover
  * Baseband - discussing adding paths for ADC data 
  * Analog - adding analog test mux, buffers, controls therefore 
    * @avi providing unity-gain test buffer from prior tape-out 
* Added TSI interface, should help de-risk CPU bring-up 
* Tape-Out date - next round after our announced one is 6/16, can catch that as fallback 
* RF team needs to be showing layout in every update from here on 

Action Items: 

* [ ] @dan - Discuss synchronization of live controls, e.g. dividers, with PLL team 
* [ ] @avi - talk to RF team about adding ref-clock bypass, for RX test w/o LO PLL 


### Fri March 19, 2021

Agenda: 

* Lectures 
  * Tuesday - Simone guest lecture
  * Thursday - either all updates, or Avi 
* Follow-up on package lecture, provide more specifics on our own chip's setup 
* Design Status 
  * RF 
    * DCO design definitely going slower than hoped
      * Encourage getting *something* rolling vs full-breadth of specs 
      * @ali & @kris getting together with Alex 
    * PLL can probably use some help 
    * Analog baseband has some layout, a bit of a head start 
  * RF Baseband 
    * Phase alignment/ CDR now in progress
    * Anson getting in & helping starting ~tomorrow 
    * Priority to get something feature-complete, get into back-end 
* Post-Semester
  * @bora sorting out budget to hire board design, post-silicon work 
  * Ideally someone associated with the course. Alex M looking for summer job.
* Tape-Out Schedule 
  * Univ shuttle was overbooked, had to move May Si to July
  * @kris reserved 2mm2 for May Muse shuttle
  * Next shuttle tape-out 9/8, likely will require waiting for this 

Action Items: 

* [x] @kris contacting Muse about moving to next shuttle 


### Fri April 9, 2021

Agenda: 

* Lectures 
  * All student updates, and likely so going forward 
* Design Updates
  * CPU - largely divert to back-end work
    * Nayiri still doing most, starting to split out work 
    * Anson, Josh, Eric Wu volunteered to start contributing
    * Line up for verif work: Daniel Fan, Cheng Cao 
  * Baseband - RTL work getting there, not "that done" yet, Ryan & Griffin staying on it
  * RF Top - Felicia & Jackson getting most (all) hooked up. No LO PLL yet.
  * RF Front End - schematics OK, layout started 
  * LO PLL - reluctantly doing stuff 
    * Remaining pieces of schematic - divider, CP leakage updates 
  * RF Analog Baseband - seems furthest along 
    * Did Leon Wu drop the class? Appears missing. 
    * Seems likely to need re-routing one of these guys to PLL 
  * Analog Top/ Power/ Bias
    * Bias network layout started 
    * LDO layout started 
* Needs
  * RF TX driver/ buffer 

Action Items: 

* [x] @avi pinging RF group on TX driver 
* [x] @dan getting Cheng, Daniel onto verification, BB-RF interaction 


### Fri April 16, 2021

Agenda: 

* Lectures 
  * All student updates, and likely so going forward 
  * Two more weeks of lectures 
  * Plan to continue meeting, same times, during reading week 
* Design Status 
  * PLL - probably furthest behind. Stay on em. Discussed going open-loop, probably too risky that it'd work. 
  * Analog baseband - good layout progress, probably need them to contribue up-hierarchy. Re-direct Kerry & Jeffrey to its top layout. 
  * RF Top-Level - push this to Shreesha 
  * Integration - pad ring in LVS, not much else. 
    * Free up Jackson to contribute some more here. 
    * Kareem working LVS on pad-ring, hopefully can contribute to top
    * Troy, Dylan struggling
  * Digital 
    * LVS is clean 
    * DRCs - fixed via1, single-site gap, looking reasonable 
    * Remaining DRCs - via4 enclosure, random vias, 
    * Baseband - debugging, finding bugs, squashing bugs, Ryan & Griffin to stick with this. Anson helping. Move to help verify core next week. 
  * Digital-Side Assignments 
    * Nayiri - driving back-end work 
    * Eric Wu - lots of back-n-forth on gate-level sims 
    * Others on back-end - Josh, Anson (some) 
    * Cheng - working out digital top level, IO controls, reset sync
    * Daniel Fan - has said he's still doing AES software thus far. Reiterate need mixed verification instead. 
* Leon Wu - remains missing 

Action Items: 

* [x] @avi sit down with Troy/Dylan, get them started on LVS & debug thereof 
* [x] @dan reiterate with Daniel Fan, get on mixed-signal verif 
* [x] @dan reminding of PLL bypass path 


### Fri April 23, 2021

Agenda: 

* Lectures 
  * Same design meeting format from here 
* Design Status 
  * Baseband - latest-forming digital part. Reviewing immediately after this. 
  * Where is that digital top-level cell? With the synchronizers etc. 
  * LO PLL - lots left to go, putting together top-level schematic, block-level layouts
* Tape-out quality metrics
  * Corners - research chips have generally been getting very close to TT, how important are these? Less than in real life. 
  * Starting to evaluate PLL late-drop-in 
  * Chip finishing - seal ring, pad DRCs OK, would need fill / density 
    * Density fill tends to screw up on resistors, OD fill, should be relatively quick fix
  * Pad-frame layers DRC clean
* To Do a 4/28 Drop to Muse:
  * Weds 4/28 @ 11:59pm - GDS to FTP server
  * Tues 4/27 EOD - full GDS to fill, debug density, write up DRC waivers 
  * Mon 4/26 - Digital layout into Virtuoso, Chip-Level LVS & DRC 
  * Gotta have all device-types down, notably including *inductor* 

Action Items: 

* [ ] @avi trialing fill, sending typical fixes 
* [ ] @dan sending this mad-rush tape-out schedule 


### Lecture Topics Backlog 

* Avi on Verilog-A, testbenching, structured analog design 
* Zhaokai BAG ADC
* SV Test-benching, assertions
* @ali (or delegate) - ESD & latch-up
* @bora - baseband 
* @ali - OCEAN/ SKILL/ other Cadence-scripting
* More on timing analysis, debugging thereof 
* Testing / bring-up / lab intro. Packaging, off-chip interfaces, PCB, equipment etc. 




