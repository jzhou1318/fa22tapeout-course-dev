
# Design Schedule Milestones 

Our schedule starts at its end: we'll be sharing silicon with a number of other projects on 
[Muse Semi's May Shared-Block Tapeout](https://www.musesemi.com/shared-block-tapeout-schedule). 

We'll cover our milestones accordingly: starting from the end. 

### Full-Chip and Final Layout

The last stages of our schedule include a few steps of back-and-forth with our foundry partners. 

**Final layout** is exactly that: the date after which our layout will not change, 
absent urgent demand from our foundry partners. (And we do not want to field such feedback.) 
This will incude a preceding week in which Muse has our ostensibly-final layout, 
and can offer DRC and other feedback. 

We'll provide that ostensibly-final layout as part of Muse's **Trial** milestone, set one week earlier. 
This will be the GDS we intend to tape-out, potentially with caveats or questions about its more subtle design rules. 

Muse's listed **Tape-Out**, a week after final layout, will only be relevant if they have bad news for us. 
Otherwise, final is final, until wafers ship back to us months later. 

### Final Sub-Block Layout 

Prior to having a clean chip-level, we'll need LVS and DRC-clean layouts of each major sub-block. 
(Digital from PnR, RF, any remaining analog.) 
On this date final GDSes for everything but the chip's top-level are due. 
After this date only the integration-level layout should be in progress. 
Everyone else will be working on some form of verification. 

### RTL & Schematic Freeze 

A few weeks before finalizing sub-blocks' layouts, we'll need to finalize their *front-end* design. 
This comprises their RTL for digital circuits, and schematics for analog. 
This enables verification and integration work against a locked front-end implementation. 
After this date all work will be either on physical design (layout) or verification. 

### Mock Tape-Out 

### Interface Lock 

### Preliminary Schematics & RTL 

### Preliminary Interfaces, Specs, & Floor-Plans 


--- 

In addition to all of these milestones, we'll hold a design review with a number of our industry partners, 
around the time of the Spring Break. Take the opportunity to present your work, take their questions and advice! 


