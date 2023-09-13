# Computer-Vision-and-Machine-Learning-for-Bioengineering-Applications

This repository contains details and materials for the tutorial entitled "Computer Vision and Machine Learning for Bioengineering Applications" at ICIAP2023 

# INTRODUCTION AND MOTIVATION 

In the last few years, **Computer Vision (CV)** and **Machine Learning (ML)** algorithms have been applied to a high number and variety of application scenarios, highlighting good performances in solving different tasks. State-of-the-art ML algorithms are exploited in many tools commonly used in everyday life (e.g., social networks, streaming services).
**The application of these algorithms in the biomedical domain has been only partially explored**.
Biomedical engineering consists in the application of fundamental theories and analytical practices to medicine and biology. Research in this field is essential for a broad range of applications, including the development of diagnostic expert systems. Biomedical data are typically high-dimensional, diverse and irregular. For these reasons, developing CV and ML algorithms effective and accurate in this domain is challenging and it requires the design of ad-hoc approaches able to solve classical problems (e.g., features detection, segmentation, anomaly detection) with new perspectives. **Employing these algorithms in this domain may be effective for data analysis and automatic diagnosis**.
Human motion and microscopic image analysis represent two important examples of problems where CV and ML methods have been exploited with promising results, with peculiar features requiring specific solutions. The open challenge consists in developing systems suitable for routine clinical use, providing open-source tools fundamental for diagnosis support.

In the last few years, it has been a growing interest of the computer vision community towards bioengineering data. The reason for this interest is that biomedical data present particular challenges that open new research directions. Applications of interest include: automatic diagnosis, human-robot interactions, human motion characterization, rehabilitation and synthetic biology. In this tutorial, we will focus on two emerging fields of application: A) **video-based human motion analysis** and B) **anomaly detection framework for microscopic cell analysis**.

# PART A: Video-based human motion analysis

In the first part of this tutorial, we explain and provide guidance for all the steps necessary to perform markerless gait analysis. Gait analysis is a fundamental tool in medicine and rehabilitation. It helps expert physicians to characterize and monitor motion patterns after orthopedic injuries and in people with neurological diseases. Infrared marker-based motion capture systems (MoCap) have been developed to track continuous motion in the 3D space. Due to their high level of precision, infrared marker-based systems are considered the gold standard in modern gait analysis. However, these approaches have limitations. First of all, they require many markers to be attached firmly to the body of the person. This process is time consuming and expensive, resulting in a cumbersome setup that can influence the naturalness of the motion. Also, these systems require skilled personnel to apply the markers correctly and to post-process the recorded data, making the overall analysis operator dependent.
Markerless video-based gait analysis has been recently proposed as an alternative to marker-based systems since it does not require expensive and cumbersome setup. The challenges presented in this field are the high data variability and the high level of accuracy required. 
In this tutorial, we discuss the step-by-step process to perform markerless video-based gait analysis on a given video example.

1. **Detection of keypoints on the human body**. To achieve this task, we leverage VisionTool, a deep learning-based semantic feature detector that can detect body parts from videos after an appropriate fine tuning. At the beginning, we label a small set of images with the points of interest (hip, knee, ankle and foot).
Then, we train a deep learning architecture with the aim to learn to identify them. We select one of the pre-trained models available in VisionTool.
2. **Video analysis**. Once the keypoints are labeled and the selected architecture is trained, we input the whole video to our fine tuned model and we detect the selected keypoints in all the frames composing the video. 
3. **Filtering**. The landmarks trajectories are then filtered to reduce possible mispredictions.
4. **Quantitative parameters extraction**. The filtered trajectories are used to extract quantitative parameters that can describe the motor task, such as: (i) gait speed, computed by estimating the displacement of keypoints over time; (ii) cadence (i.e., the number of steps per minute); (iii) step length, computed by measuring the distance between the feet landmarks while they are touching the ground; (iv) the duration of swing and stance phases, identified respectively with the time during which the foot is or is not in contact with the ground.

link to videos and materials: https://www.dropbox.com/sh/8qkfxedp97z8jzz/AACUM2t0AH__ZwIxxh-2O072a?dl=0
Colab notebook: https://colab.research.google.com/drive/1pHbwSYrKMYSAufmi2J1SY_TUPL56_Hz7?usp=sharing

# PART B: Anomaly detection framework for microscopic cell image analysis 

In the second part of this tutorial, we will implement an anomaly detection framework for the analysis of microscopy cell images.
We will implement three main steps:

1. **Image processing and deep learning based segmentation**. We will segment the cell body from the background of the image for the next step.
2. **Descriptors engineering**. We will engineer a set of descriptors for our cells;
3. **Anomaly detection**. We will implement anomaly detection algorithms for the classification of in- and out-of-class samples, based on the descriptors engineered in the second step.
  
As a test dataset, we will use an open source dataset containing 6400 images belonging to 10 different species of freshwater plankton.
The dataset has been released in [1]. 

For this tutorial, we select a subset containing five species, as shown in Fig. 1. 

![DATASET](https://github.com/Malga-Vision/Computer-Vision-and-Machine-Learning-for-Bioengineering-Applications/assets/51142446/59be2724-4906-44f4-89c1-b861a42ab268)

**Figure 1. Sample images of the five species considered in this tutorial. From the left to the right: ACTINOSPHAERIUM NUCLEOFILUM; PARAMECIUM BURSARIA; VOLVOX; SPIROSTOMUM AMBIGUUM; STENTOR COERULEUS.** 


[1] Pastore, V. P., Zimmerman, T. G., Biswas, S. K., & Bianco, S. (2020). Annotation-free learning of plankton for classification and anomaly detection. Scientific reports, 10(1), 12142.
https://ibm.box.com/v/PlanktonData

Colab Notebook: https://colab.research.google.com/drive/1x_SXvv66Yx2ab5l6-Rg2U5ZbK1PLKyJn?usp=sharing
