### Fiber Photometry data analysis for dual color recordings with a TDT System

The purpose of this Jupyter notebook is to analyze Fiber Photometry Data recorded by a TDT system

The notebook is  adapted from  Thoam Akam & Lauren Burgeno by referring to [Simpson et al. 2023](https://www.sciencedirect.com/science/article/pii/S0896627323008905)

The preprocessing consists of the following steps:

  1. Lowpass filtering to reduce noise (10 Hz filter).

  2. Correction for photobleaching, over time. A double exponential fit is utilized for this purpose.
  
  3. Movement correction by subtracting a linear fit of the movement control channel.

  4.  Z-scoring of the data
    
  5. Alignement to a selected event

You can find an [example file](0934-241017-143128) for a dual color recording of PinkyCaMP and sDarken attached. 
The recording was done in the prelimbic area. PinkyCaMP is expressed in pyramidal neurons and sDarken in all neurons.
