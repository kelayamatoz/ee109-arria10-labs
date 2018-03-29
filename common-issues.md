## FAQs

### Running into Issues When Regenerating Design
Sometimes it is possible that you change your design multiple times and want to
generate bitstream for every single iteration of them. Currently we do not have
a mechanism for version control. If you made some changes to your old design and
want to regenerate the design files, you should either remove the old design
folder in `./gen`, or put your changes into a new design and name it
differently. 

### Observing Error Information about Spatial IR when Running Bitstream Generation
Sometimes when running `make vcs` or `make $TARGET`, you would observe some errors that look like: 
```bash
[error] /home/tianzhao/ee109-teaching/spatial-lang-ee109/gen/DotProduct_1_1_16_Int/chisel/x1279.scala:10: not found: value x1278
[error]   x1278.r := (b704 + 16.FP(true, 32, 0)).r
[error]   ^
[error] /home/tianzhao/ee109-teaching/spatial-lang-ee109/gen/DotProduct_1_1_16_Int/chisel/x1279.scala:10: not found: value b704
[error]   x1278.r := (b704 + 16.FP(true, 32, 0)).r
[error]               ^
[error] /home/tianzhao/ee109-teaching/spatial-lang-ee109/gen/DotProduct_1_1_16_Int/chisel/x1296.scala:10: not found: value x1295
[error]   x1295.r := (b735 + 16.FP(true, 32, 0)).r
[error]   ^
[error] /home/tianzhao/ee109-teaching/spatial-lang-ee109/gen/DotProduct_1_1_16_Int/chisel/x1296.scala:10: not found: value b735
[error]   x1295.r := (b735 + 16.FP(true, 32, 0)).r
...
```
This usually happens because you have an old design generated from Spatial, and when creating the new design you forgot to remove the old design. You can resolve this issue by removing the old design and regenerate it. 

### Could Not Find the Generated Bitstream
This is usually due to the fact that your design is so large it cannot fit on
board. You can find a few reports under the verilog-arria/output_files folder of your
generated design directory, which can tell you if your design is too large. 
