### Laboratory Exercise 2: Advanced Usage of Spatial
In the last lab, we went through the basics of Spatial. In this lab, we are going to explore more advanced features of Spatial.

We will first go through the usage of more advanced controllers. Then we will use the controllers to build an app that performs matrix multiplication. After we the app, we will learn about how to improve the performance of your app by making it parallel. We will also learn about how to use the tools Spatial provides to optimize the application.

More specifically, we will be covering the usage of the following elements: 

Controllers: MemReduce, MemFold, FSM

On-Chip Memories: RegFile, LUT, ShiftRegister, LineBuffer

## MemReduce, MemFold
MemReduce is very similar to Reduce, but different in the sense that Reduce operates on a register while MemReduce operates on a piece of on-chip memory (SRAM). If we take a step back and try to understand the two controllers from an abstract level, we will see that Reduce is a controller for scalars and MemReduce is for tensors. 

Here is the syntax for 
