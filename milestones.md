
# Design Schedule Milestones 

Our schedule starts at its end: we'll be sharing silicon with a number of other projects on 
[Muse Semi's May Shared-Block Tapeout](https://www.musesemi.com/shared-block-tapeout-schedule). 

We'll cover our milestones accordingly: starting from the end. 

### Full-Chip and Final Layout

The last stages of our schedule include a few steps of back-and-forth with our foundry partners. 

**Final layout** is exactly that: the date we provide our final layout to the foundry.
After that, absent urgent feedback from our foundry partners, we're done. 
(And we do not want to field such feedback.) 
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
After this date only the integration-level layout will be edited. 
Everyone else will be working on some form of verification. 

### RTL & Schematic Freeze 

A few weeks before finalizing sub-blocks' layouts, we'll need to finalize their *front-end* design. 
This comprises their RTL for digital circuits, and schematics for analog. 
This enables verification and integration work against a locked front-end implementation. 
After this date all work will be either on physical design (layout) or verification. 

### Mock Tape-Out 

For the final month-plus of our design we'll be iterating on working (in senses) but incomplete versions of our full-chip design. 
This is a hallmark of our *agile* approach. 

The mock tape-out will create a full-chip GDS, including the best-guess versions of each sub-system available. 
This will be a stress-test for our ability to integrate everything, pass DRC checks at boundaries between blocks, 
and verify we can craft a layout which implements our (near-frozen) front-end designs. 

### Interface Lock & Trial Integration 

Before completing the mock tape-out we'll freeze the interfaces for each sub-system. 
This includes both the logical/ behavioral interface (i.e. the ports and their actions), 
as well as the physical interface (i.e. the abstract layout as defined by a LEF). 

Trial integration will use these sub-block designs to first create a working chip-level front-end design, 
and then to create the layout for the mock tape-out. 

### Preliminary Schematics & RTL 

Our second major milestone will require initial front-end designs. 
These schematic and RTL designs will not be *final*, but should be *complete* in the sense that they: 

* Adhere to the already-defined prelim interfaces (with any caveats you work out between teams) 
* Include all sub-systems, comprehend and preferably connect all interactions between them 

Prelim front-end designs do not necessarily need to meet every parametric spec - 
but must include reasonable analysis to assure you *can* meet specs, 
under your area budget and power targets. 

### Preliminary Interfaces, Specs, & Floor-Plans 

Among our first milestones will be defining how our major subsystems interact and talk to one another. 
As we've reviewed in covering a [hierarchical design flow](./notes), this will include their port-interfaces, 
along with (at this point) general descriptions of what how those interfaces are used, 
and how they might be connected in physical layout (i.e. to a chip-level pad, versus to an on-die register). 

Both the chip-level and each sub-system will need a paired floor-plan diagram, 
illustrating its rough placement, area allocation, and general plans for routing between its sub-blocks. 

These preliminary interfaces will be the basis for all work at all levels of hierachy above. 
Note no *internal* design need necessarily be provided - but boundary information is a must. 


--- 

In addition to all of these milestones, we'll hold a design review with a number of our industry partners, 
around the time of the Spring Break. Take the opportunity to present your work, take their questions and advice! 


