## FAQs

### Running into Issues When Regenerating Design
Sometimes it is possible that you change your design multiple times and want to
generate bitstream for every single iteration of them. Currently we do not have
a mechanism for version control. If you made some changes to your old design and
want to regenerate the design files, you should either remove the old design
folder in `./gen`, or put your changes into a new design and name it
differently. 

### Does Not Find the Generated Bitstream
This is usually due to the fact that your design is so large it cannot fit on
board. You can find a few reports under the verilog-arria/output_files folder of your
generated design directory, which can tell you if your design is too large. 
