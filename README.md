# Computer-Vision-and-Machine-Learning-for-Bioengineering-Applications

This repository contains details and materials for the tutorial entitled "Computer Vision and Machine Learning for Bioengineering Applications" at ICIAP2023 

# INTRODUCTION AND MOTIVATION 

In the last few years, Computer Vision (CV) and Machine Learning (ML) algorithms have been applied to a high number and variety of application scenarios, highlighting good performances in solving different tasks. State-of-the-art ML algorithms are exploited in many tools commonly used in everyday life (e.g., social networks, streaming services).
The application of these algorithms in the biomedical domain has been only partially explored.
Biomedical engineering consists in the application of fundamental theories and analytical practices to medicine and biology. Research in this field is essential for a broad range of applications, including the development of diagnostic expert systems. Biomedical data are typically high-dimensional, diverse and irregular. For these reasons, developing CV and ML algorithms effective and accurate in this domain is challenging and it requires the design of ad-hoc approaches able to solve classical problems (e.g., features detection, segmentation, anomaly detection) with new perspectives. Employing these algorithms in this domain may be effective for data analysis and automatic diagnosis.
Human motion and microscopic image analysis represent two important examples of problems where CV and ML methods have been exploited with promising results, with peculiar features requiring specific solutions. The open challenge consists in developing systems suitable for routine clinical use, providing open-source tools fundamental for diagnosis support.

In the last few years, it has been a growing interest of the computer vision community towards bioengineering data. The reason for this interest is that biomedical data present particular challenges that open new research directions. Applications of interest include: automatic diagnosis, human-robot interactions, human motion characterization, rehabilitation and synthetic biology. In this tutorial, we will focus on two emerging fields of application: A) video-based human motion analysis and B) anomaly detection framework for microscopic cell analysis.

# PART A: Video-based human motion analysis 

More details to be released soon 

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



The second part of this tutorial will be released soon as a jupyter notebook. An introductory presentation will be released soon as well. 
