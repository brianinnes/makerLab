# Workflow for creating PCB

## Design the PCB

Use KiCad to create the schematic then layout the board.  Whilst laying out the board there are some limitations that need to be taken into consideration:

- the width of the cut when separating copper traces is dependant on the bit and the depth of the cut.
    - 0.1mm deep cut with the 0.2mm 30º v-bit produces a 0.2536mm wide cut
    - 0.1mm deep cut wiht the 0.1mm 60º v-bit produces a 0.2155mm wide cut
- holes can not be drilled smaller than the size of the drill bit, so if you want 0.4mm vias, then you need a 0.5mm drill bit.  Design the board layout with the drill bits you own in mind

When you have finished designing the PCB you should export the gerber files and the drill file

The gerber files should include the copper, mask and silk screen for each side of the board.  You also need the edge cut gerber

## Create g-code files

Use FlatCam to convert the gerber and drill files into g-code to run on the Carvera machine

!!!Todo
    Complete this section
    
## Fabricate the PCB

!!!Todo
    Complete this section