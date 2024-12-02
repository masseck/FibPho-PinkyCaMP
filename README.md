### Fiber Photometry data analysis for dual color recordings with a TDT System

This Jupyter notebook [Fiber-Photometry-Analysis-PinkyCaMP](Fiber-Photometry-Analysis-PinkyCaMP.ipynb) is designed to analyze fiber photometry data recorded using a TDT system.

The notebook builds on methods adapted from Thomas Akam and Lauren Burgeno, with reference to [Simpson et al. 2023](https://www.sciencedirect.com/science/article/pii/S0896627323008905)

The preprocessing pipeline includes the following steps:

1. Lowpass Filtering: A 10 Hz lowpass filter is applied to reduce high-frequency noise in the signals.

2. Correction for Photobleaching: A double exponential fit is used to correct signal drift caused by photobleaching over time.

3. Movement Correction: Artifacts due to movement are removed by subtracting a linear fit of the movement control channel from the signal.

4. Z-Scoring: The data is normalized using Z-scoring to facilitate comparisons across recordings.

5. Event Alignment: Signals are aligned to selected events for further analysis.
   
6. Data can be are stored as a csv file

An [example file](0934-241017-143128) is provided for a dual-color recording of PinkyCaMP and sDarken. 
The recording was performed in the prelimbic area of the brain, where PinkyCaMP is expressed in pyramidal neurons and sDarken is expressed in all neurons.

### Combining Multiple Recordings for Summary Plots and Heatmaps

Building on the preprocessing and analysis, multiple fiber photometry recordings are combined [in this Jupyter notebook](Fiber-Photometry-combined-analysis.ipynb) to generate summary plots and heatmaps for group-level analyses. 


