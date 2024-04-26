# EEG-Fear-Detection
This repository contains data, and code for our Brain-Computer-Interface (BCI) project for the 2023-2024 season of Neurotech@Davis. The project aims to explore how different frequencies of brainwaves behave when exposed to a scary stimulus. To do this, we tracked brain activity closest to the amygdala, and then seperated the trials by stimulus type (relaxed or scary), and then further subdivided it by band of interest (beta, theta, delta).

# Aim:
The repository aims to provide open-source code for processing EEG signals relating to fear. All code files may be used, but please let us know (we want to see our work in action!). The code should empower researchers and developers to make advances in fear detection, and their understanding of how fear works in the brain.

# 1. Data Collection:
The project involved placing 8 EEG electrodes on specific positions on the subject's head to read neural signals. The OpenBCI hardware and software were used to record the raw data. Data collection involved particpants watching a ten minute video that would alternate between relaxed clips (R) and scary clips (S) such that there would be six different sections in the whole video (RSRSRS).

# 2. Preprocessing:
After we had collected the data, we proprocessed it to eliminate noise and artifacts. This involved applying a band-pass filter to retain beta, theta, and delta wave frequencies, applying IIR filters to enhance the signal of interest, and using a notch filter to remove power grid interference.Once we had filtered data, we cut out the different sections from the video. From here, we averaged out all the scary-state data and did the same for the relaxed-state data. Finally, we graphed it out to gain further insight.

# 3. Evaluation and Results:
After collecting data, and processing it, we noticed an interesting difference between the beta waves, and the theta and delta waves. Plotting the power spectral density graph of the latter two, we notice that existing frequencies only become stronger, this trend did not occur with the beta waves. Taking a look at the beta-relaxed graph, we can see frequencies in the >12.5 Hz range are already elevated. Once our participant is exposed to the scary stimulus, the band “inverts”, and frequencies that were inactive before become active, and vice versa. From these findings, we can conclude that while these three bands are all strong correlates of fear, the beta band has its own unique behavior. We currently do not have any suspicions as to why this phenomena occurs.


# 5. Possibilities and Limitations:
Given our results, we hope to have laid foundational research for developing neural “kill-switches”. Through our data, researchers of these mechanisms will know what behaviors to look for. A limitation of this project was recording accurate data due to equipment and the location of the part of brain that we wanted to observe. Not only would better equipment make this endeavor much more accurate, but considering a switch from surface level EEG to invasive EEG would prove much more effective albeit a rather aggressive approach. 

# 6. Acknowledgements
Special thanks to the Neurotech@Davis Projects board members, especially Adit and Dhruv, for helping us get the code into place. WIthout them, this project wouldn't be anything close to where it is now.
