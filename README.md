## Uploaded by Haohan Wang
## KAGGLE LINK :https://www.kaggle.com/wanghaohan/confused-eeg## Description
HAOHAN:We collected EEG signal data from 10 college students while they watched MOOC video clips. We extracted online education videos that are assumed not to be confusing for college students, such as videos of the introduction of basic algebra or geometry. We also prepare videos that are expected to confuse a typical college student if a student is not familiar with the video topics like Quantum Mechanics, and Stem Cell Research. We prepared 20 videos, 10 in each category. Each video was about 2 minutes long. We chopped the two-minute clip in the middle of a topic to make the videos more confusing. The students wore a single-channel wireless MindSet that measured activity over the frontal lobe. The MindSet measures the voltage between an electrode resting on the forehead and two electrodes (one ground and one reference) each in contact with an ear. After each session, the student rated his/her confusion level on a scale of 1-7, where one corresponded to the least confusing and seven corresponded to the most confusing. These labels if further normalized into labels of whether the students are confused or not. This label is offered as self-labelled confusion in addition to our predefined label of confusion.

These data are collected from ten students, each watching ten videos. Therefore, it can be seen as only 100 data points for these 12000+ rows. If you look at this way, then each data point consists of 120+ rows, which is sampled every 0.5 seconds (so each data point is a one minute video). Signals with higher frequency are reported as the mean value during each 0.5 second.

EEG_data.csv: Contains the EEG data recorded from 10 students

demographic.csv: Contains demographic information for each student

video data : Each video lasts roughly two-minute long, we remove the first 30 seconds and last 30 seconds, only collect the EEG data during the middle 1 minute.

Acknowledgements
Wang, H., Li, Y., Hu, X., Yang, Y., Meng, Z., & Chang, K. M. (2013, June). Using EEG to Improve Massive Open Online Courses Feedback Interaction. In AIED Workshops. [PDF]
The data is collected from a software that we implemented ourselves. Check HaohanWang/Bioimaging for the source code.

Inspiration
This dataset is an extremely challenging data set to perform binary classification. Here are some recent classification results for reference:

SVM: 67.2%
Bi-LSTM (Ni et al 2017): 73.3%
CF-Bi-LSTM (Wang et al 2018): 75.0%
It is an interesting data set to carry out the variable selection (causal inference) task that may help further research. Past research has indicated that Theta signal is correlated with confusion level.

It is also an interesting data set for confounding factors correction model because we offer two labels (subject id and video id) that could profoundly confound the results.
