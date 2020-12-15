
# Non-Published Stuff Here! 

Keeping this in the `_private` directory (or any directory beginning with `_`, `.`, and 
[a few other special characters](https://jekyllrb.com/docs/structure/)) 
will keep it from being published as part of the site. 

---

## Planning & To-Dos 

### Tues Dec 8, 2020

* Wrote initial, very rough, early part of schedule 
* [x] Invite Kris, Ali to this group 
* [ ] BWRC Accounts for all students 

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

* [ ] @bora working with BWRC staff on student NDAs/ access for TSMC28. ETA this week. 
* [ ] @bora providing links to ADC & DAC generators he wants to use 
* [ ] @ali join https://github.com/ucberkeley-ee290c 
* [ ] @bora setting up Piazza, will use for initial student backgrounds/ interests poll 
* [ ] @dan will write up said poll

