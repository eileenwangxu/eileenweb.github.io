---
title: "GymBand: Adaptive Music Recommendation for Heathier Fitness"
meta_title: ""
description: ""
date: 2023-05-31T05:00:00Z
image: "/images/run.png"
categories: ["Projects"]
author: "Team"
tags: ["System Design"]
draft: false
---
We aim to help runners achieve running goals in a positive emotion and healthy state by music aid. We analyzed ECG and IMU signals captured from runners to determine their physiological status and emotional valence, then utilized music recommendation strategy based on beat control and emotional V-A model regulation. 

### 1. Background

Based on our observations, many people run for fitness and prefer to listen to music to relieve fatigue and boredom. However, there are still problems with playlist selection, running rhythm control, state holding, and so on.

When we go on long-distance running, music has many functions. Firstly, it helps maintain a healthy status, including a suitable heart rate, high HRV_SDNN, and a faster cadence. Greater HRV_SDNN suggests better recovery and is more receptive to further training stress. A faster-running cadence changes the positioning of where the foot lands compared to a lower cadence. It will limit the force with which the human body hits the ground. Maintaining a healthy status can improve fat-burning efficiency and reduce the pressure on our joints.
Secondly, music also aids in emotion regulation. Listening to music while exercising reduces physical exertion, improves endurance, and brings positive emotion to the runner. Research shows that listening to music whilst exercising diminishes the rate of perceived effort by 12% and enhances endurance by 15%.

So we believe that the basis of healthy exercise is maintaining a suitable heart rate and running cadence, also staying in a positive mood. To achieve this goal, we chose to use adaptive music to stimulate and adjust heart rate by tempo intervention and boost the performance of goal-oriented exercise through emotion arousal.

{{<image src="images/gymband/motivation.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}

### 2. Method
GymBand utilizes signal processing metrics to analyze physiological and IMU signals collected from the runner in a time-varying exercising state, from which we derive the runner's health information and emotional status. We select music databases from open-sourced datasets and calculate music clips' tempo feature (BPM) and their corresponding quadrant emotion based on the Affective Dimensional Model (ADM).

We design two filters to select suitable music for goal-oriented running. The physiology-level filter aims to map running cadence with music BPM, while the emotion-level filter arouses the runner's mood by playing relatively positive music.

{{<image src="images/gymband/system.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="w-11/12 img-fluid" title="image title"  webp="false" >}}

### 3. Experiments and results
#### 3.1 Datasets
##### EmoMusic
We constructed the recommended music library of Gymband from EmoMusic Dataset. EmoMusic selected 1000 songs from Free Music Archive (FMA). Some redundancies were identified, which reduced the dataset down to 744 songs. The extracted 45 seconds excerpts are all re-encoded to have the same sampling frequency, i.e, 44100Hz. Each excerpt has been scored a Valence value and an Arousal value, which were used to classify these excerpts into four categories: HVHA, HVLA, LVHA and LVLA.

##### DREAMER
We utilized DREAMER dataset to train our human emotion classification model based on ECG signals. DREAMER contains data collected from 23 participants, with 18 samples each. The stimuli used were video clips ranging from 1 to 3 min, with the focus on the ECG and EEG modalities. The ECG device used was a low-cost, wireless, portable, and wearable off-the-shelf device from Shimmer. The sampling rate was 256 Hz, with two-lead and three-lead configurations. Self-annotation of the subjects was conducted using a valence, arousal, and dominance ADM.

##### Self-collected Dataset
In order to implement GYMBAND music recommendation system, we collected multimodal data during running by ourselves. Due to the obstruction of the COVID-19 epidemic, we only collected the data of two people, namely Ruiqing Wang and Ziqi Gao, members of the group. Ruiqing Wang and Ziqi Gao ran on the indoor treadmill and the outdoor track respectively.
{{<image src="images/gymband/01.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}

#### 3.2 Impact of Music BPM on Running cadence
In order to explore the impact of different BPM music on the runner's cadence, Ziqi Gao listened to music with similar emotions at three different BPMs during the same distance running. The results showed that, within a certain range, the faster the music, the faster the pace of the runners.
{{<image src="images/gymband/02.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}

#### 3.3 Impact of Music on HR and HRV_SDNN
The figure bellow shows Ruiqing‘s heart rate features while running under different conditions. We utilized these features to calculate her HRV-SDNN while running with music, and the results show that music with positive emotions during running can help improve HRV_SDNN, which promotes the heart health of runners.
{{<image src="images/gymband/03.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}

The figure bellow shows Ziqi's heart rate changes while listening to music with different BPMs, which reveals that higher music BPM will lead to a higher heart rate in runners.
{{<image src="images/gymband/04.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}

#### 3.4 Impact of Musical Emotion on Runners' Emotion
We utilized the trained machine learning models to calculate the emotion distribution of Ruiqing while running with different musical emotions. The results in the figure shows that when listening to more positive music, the runners' mood was more positive and stable, which was conducive to their achievement of established exercise goals.
{{<image src="images/gymband/05.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}

### 4. Dicussion and Conclusion
The Goal of GymBand is to help runners achieve running goals in a positive emotion and healthy state by music aid. To be more specific, a positive emotional state means a high valence and high arousal mood. An ideal physical state includes a high running cadence, a healthy heart rate, and a higher HRV_SDNN value.

The recommendation strategy of Gymband is based on beat control and emotion regulation. A high BPM of music improves the stride frequency of the runner, helping them to maintain a healthy heart rate. Also, music with higher emotional valence and arousal can help runners improve HRV_SDNN, helping their emotions during exercise remain positive for a longer time.

Affected by COVID, we have very few participants and data. Secondly, WITMOTION and Polar H10 sometimes are disconnected, causing failed data collection. Thirdly, the system now is running offline, so in the future, we plan to implement online real-time recommendations. Besides, we will collect more data from various participants and different age groups. Predict physiological status and emotional valence in advance to improve our recommendation mechanism, and also consider diverse factors, such as how to recommend interventional music to improve the runner's state when running at an exhaustion state.

