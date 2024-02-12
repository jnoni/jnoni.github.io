---
layout: post
title: Studying Attentional Blink and Neural Correlates of Motion Processing
subtitle: Neuroscience | Master's Thesis
bigimg: /img/path.jpg
tags: [computer science, neuroscience, thesis]
---
In this post, I give a glimpse of my Master's study and what experiments I carried out and their inferences. Feel free to reach out to discuss more.

## Abstract:
When two targets among distractors are presented close in time (200-500ms), processing of the second target (T2) is impaired, provided the first target (T1) is correctly identified. This phenomenon known as attentional blink has been tested with an array of stimuli, mostly static like letters and digits. However, very few have studied attentional blink with dynamic stimuli like random dot patterns (RDP). Given dynamic stimuli are integrated over space and time, we want to test how RDPs are processed under capacity limited conditions over time and measure the corresponding neural correlates through EEG.

## Introduction
In the simplest of visual activities such as reading a book or watching a video, our eyes briefly fixate in a certain visual space and gradually make a move between fixation points. This happens as our brain goes through visual processing deficit or suppression during rapid eye movement temporarily. Limitations that impact the capacity of our brain to attend to and process a series of visual information/stimuli can be studied using Rapid Serial Visual Representation (RSVP) paradigm. There have been studies in the past that, through RSVP, tried to simulate and study this temporary suppression in our visual processing, called attentional blink. However, all the past research has studied the stimuli that are static in the spatial domain. Would it be applicable to dynamic stimuli like motion stimuli as well? In this research, we design and execute an experiment to understand the attentional suppression and information integration over space and time for dynamic stimuli and analyse the time series data to present a trend.

Since in this paper, we analyse signals coming from different parts of the brain, we begin with an overview of how different compartments in brain are engaged in processing a stimuli:

- **Occipital Lobe**: This part is the primary visual processing center that helps us perceive color, motion. All the things we see are being processed here. 
- **Parietal Lobe**: It integrates information from external sources as well as internal sensory feedback from skeletal muscles, limbs, head, eyes, etc to a coherent representation. Example: eye-hand coordination.
- **Temporal Lobe**: It is associated with processing sensory input (auditory or written speech) to understand meanings using visual memories, language and emotional association.
- **Frontal Lobe**: Involved in decision making, planning, and conscious thoughts. Example: voluntary movements of all of our limbs and eyes.

We took Raymond’s “**_Temporary suppression of visual processing in an RSVP task: An attentional blink_**?” as our base paper. 

## Procedure: 
For Dual task, the subject was asked to identify a distinctively black coloured letter embedded in a stream of white letters and also to respond to the absence/presence of an ‘X’, a simple and fully specified probe. In control condition i.e the single task, no target detection was asked, only to identify an X, if present.

Probe-detection data from experimental conditions suggests that post target processing deficit significantly impacts the detection of a fully specified task.

Observations from Raymond’s experiment:

- Probe-detection data from experimental conditions suggests that post target processing deficit significantly impacts the detection of a fully specified task.
- In comparison of trends in the two conditions, experimental and control, the deficit is attentional. **Why**?
    - It’s because, in both the conditions, black target was present nonetheless, the participant's visual system was simulated by the one-black-rest-white the same way in both the cases. 
    - As no post-target deficit was observed in control condition, then the deficit in experimental cannot be due to low-level visual transients produced by the black target. It comes from an attentional blink.
- As we can observe, in experimental, probe-detection performance was high in case of SOA (stimulus onset asynchrony). It indicates that switching tasks was accomplished in a short time period.

As we have observed above, Raymond’s paper consisted of a series of experiments all centered around tweaking the post-target across time and observing the attention. Spatial attention was held constant.
Our aim with this project is to study these correlations with motion stimuli.

## Our Hypothesis: 
If two similar directions are presented close in time they will be integrated to strengthen the signal to noise ratio.

## Method

**Subjects**: Twenty seven college students were recruited from the Allahabad University. All participants’ trials were conducted after prior practice sessions, to mitigate the possibility of good results due to increasing predictability of the experiments. Participants were informed about the experiment and the purpose of the study prior to participation and an informed consent was procured. All experimental procedures were approved by the ethical board of Allahabad University.

**Stimuli**: Stimuli was designed and presented using Psychtoolbox 3.0.1 with Matlab 2012a on a Samsung monitor (frame-rate 120Hz) in Windows 7 operating system.

**Participant Recruitment conditions**: The aim of this study is to study neural correlates of attention. We ensured to account for and eliminate the possible confounding factors that might introduce bias in the study. Factors like, left/right handedness, age, vision loss with eye/frequent blinking, motor inhibition, pre-trained or not, etc. Hence, it was made sure that the population of recruitment is within 18 to 30years of age, because with age out attention capabilities are impacted. All study subjects had corrected-to-normal visual sensitivity. It was ensured that participants are healthy, not under medication with regards to physical limitations. 

## Data Collection
**Each participant underwent 400 trials for each of the four scenarios** as listed below:
- When no second target (T2, white dot pattern) is present in the stream moving in a particular direction.
- When there is a second target in the stream, the (white) pattern moves in a particular direction, with respect to the first target pattern.

Once a trial is finished, participant gives answers to the following three responses:
- Direction of the first target (white random dot pattern)
    - Right
    - Left
- Whether or not the second target pattern (random white dot pattern) is present or not? (“No Target” shown by green color)
- If yes, direction of the second target (white random dot pattern) w.r.t. the first target
    - Same direction (Blue)
    - Opposite (Black)
    - Perpendicular (Red)

## Inferences

- Observations from our experiment very significantly demonstrate the role of attention in the temporal domain for processing of motion stimuli.
- The closer the two similar directioned target streams are posed to the user closer in time, the more likely it is that the participant will be able to perceive them correctly.
- When there is a “**_temporal break_**” in presentation of the two target streams, especially for the opposite/perpendicular directions, the participant’s attention improves in perceiving and reporting the spatially different/opposing directions.
- In an RSVP Task, participant’s ability to identify the second target has a strong association with the pattern and time-proximity from the first target.
- Such a behavioral observation also verifies that humans are inherently good at making **predictions and identifying patterns** (here pattern is the directions of the streams with respect to each other.) They try to fit pieces into puzzles, which is directly related to such a high performance with same direction targets when displayed close to one another in time and the low performance for other directions.
- An unusually high performance with only single target identification can be understood from two phenomena:
    - There was no element of “interference” or “cognitive burden” on the participant to perceive, process, identify, match (with previous target T1), remembering, and reporting the target when the 2nd target stimuli is missing.
    - It is important for a researcher to account for the possibility of “pre-training” bias that can make its way into the experiment. As the trials were increased per participant, the participants might figure out patterns in each trial and try to relax their cognition with time.
- No significant difference across SOA for same condition. 
- Performance @SOA1 significantly less than SOA 2 & 3 for Opposite and Perpendicular
- In agreement to our hypothesis that, no T2 post-target processing deficit when the two targets are projected closer in time (SOA 1) and in same direction.
- Thus, it hints at two stimuli being integrated over time when projected in a similar manner.
 
## Conclusion
As alpha suppression is more evident in the same direction as compared to opposite and perpendicular, attention is acting where it is actually helping in integrating the two motions which is leading to the better perception of T2. Although the results are not strictly conclusive yet, they provided us a direction to go ahead with, a trend that’s worth noting and hinting towards our hypothesis.

## Applications
I can envision this study having important applications in treating Dementia and neurological disorders, among others.

## Acknowledgements
I’d like to sincerely thank Prof. Sonia Ray for guiding me throughout the work. Grateful to the participants who lent us their time for helping with the data collection. I thank Prof. Mrinmoy Chakrabarty and Prof. Anubha Gupta for their valuable feedback and evaluation.

