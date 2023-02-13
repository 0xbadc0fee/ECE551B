
# Table of Contents

1.  [PROJECT TRACKER](#org40e9739)
    1.  [PROJECT PROPOSAL](#org4601ba3)
        1.  [Purpose Questions <code>[1/3]</code>](#org230f8b1)
        2.  [Project Questions <code>[2/13]</code>](#org16d5de1)
        3.  [ROADMAP](#org8ee6329)
    2.  [STATE OF THE ART](#org1f3fa80)
        1.  [KEYWORDS:](#org46aaef8)
        2.  [Search Results:](#orgbde0272)
        3.  [Academic Papers:](#orgddaa6d0)
        4.  [Potential Data Sets](#orgad223be)
        5.  [Existing Kaggle, Jupyter Notebooks, GitHub Repo's](#orgab4afd0)
        6.  [Commercial, Industry Links:](#orgf16e6fd)
    3.  [INSTRUCTOR QUESTIONS](#orgd5b550e)
        1.  [](#org48c3346)



<a id="org40e9739"></a>

# PROJECT TRACKER


<a id="org4601ba3"></a>

## PROJECT PROPOSAL


<a id="org230f8b1"></a>

### NEXT Purpose Questions <code>[1/3]</code>

-   [-] Solving What Problem(s)? <code>[1/1]</code>
    -   [X] [#1] Save Money $

Reduce number of unexpected days downtime and limit degree of damage due to uncaught catastrophic events such as: debris intake small, debris intake large, fibre / organic material wrapping or binding, cavitation initiation (impeller coating worn off), etc.

-   [X] [#2] Save Money $$

Provide real-time, non-control channel, degree of variance from baseline operation in form of relative 'grading' or 'scoring' of each pump present in a given station (group of pumps).  Higher pump id's would receive grade or score based on last known performance upon shutdown.  Prior to startup of station, pump scores are polled and depending on how many units need to be activated the choice of pump and sequence of start up order will be chosen on a highest score wins case / switch.  Baselining and grading would be unique to a given pump station.  Different pump station locations have different system characteristics that make comparing pumps across multiple stations unlikely.

-   [ ] Deliver report & presentation for UNM ECE-551


<a id="org16d5de1"></a>

### TODO Project Questions <code>[2/13]</code>

-   [X] Q/A: ML / Detection vs Recogntion?

A:DETECTION ONLY

-   [X] Q/A: Remote vs. On-site implementation?

A:REMOTE

-   [ ]Q/A: Algorithms: SVM, NN?

should focus on locally runable algorithms, SVM?

-   [ ] Q/A: Datasets: ToyADMOS, ToyAMOS2, DCASE, PRONOSTIA, ?

-   [ ] Q/A: Processing Architecture: x86, ARM, FPGA, SoC, etc?

-   [ ] Q/A: Sensors: ultrasonic vs. audible range? / air-gapped vs. surface mounted?

-   [ ] Q/A: Intended budget level: affordable?

-   [ ] Q/A: Utilize existing client network?

-   [ ] Q/A: Utilize existing client control sys infrastructure?

-   [ ] Q/A: Utilize existing power / electrical supply vs. mobile solution?

-   [ ] Q/A: ML processing Real-Time vs Off-line // local vs. cloud?

-   [ ] Q/A: Input data format (wav, mp3, fft, etc)

-   [ ] Q/A: Output data format (text based logs, messages?)

-   [ ] Q/A: Bandwidth limitations; microwave, radio, fiber, etc.

-   [ ] Q/A: Working prototype or Proposed Design?


<a id="org8ee6329"></a>

### TODO ROADMAP

-   [ ] Standard Report Outline (abstract, &#x2026; , citations)
-   [ ] Abstract
-   [ ] Index Terms
-   [ ] Introduction (problem to solve, state of the art, available means)
-   [ ] Theory (hardware, software, & algorithms)
-   [ ] Methods and Materials (experiment)
-   [ ] Results (output)
-   [ ] Conculsion (did we solve a problem, future thoughts)
-   [ ] References
-   [ ] Present Final report in person / live presentation


<a id="org1f3fa80"></a>

## STATE OF THE ART


<a id="org46aaef8"></a>

### KEYWORDS:

acoustic anamoly detection, one class SVM, novelty detection, unsupervised anomaly detection, real-time, acoustic emission, ultrasonic, 


<a id="orgbde0272"></a>

### Search Results:


<a id="orgddaa6d0"></a>

### Academic Papers:

1.  A Machine Learning Approach for locating Acoustic Emissions

2.  Acoustic emmision used for detection of crack generation in propellers of turbine-pump units

3.  The application of acoustic emission for detecting incipient cavitation and the best efficiency point of a 60kW centrifugal pump: case study

4.  Machine-Learning-Based Methods for Acoustic Emission Testing: A Review

5.  Acoustic Anomaly Detection in Additive Manufacturing with Long Short-Term Memory Neural Networks

6.  Acoustic Anomaly Detection of Mechanical Failures in Noisy Real-Life Factory Environments

7.  Validation of artificial neural networks to model the acoustic behavior of induction motors

8.  A comparison between psychoacoustic parameters and condition indicators for macinery fault diagnosis using vibration signals

9.  Psychoacoustic approach for cavitation detection in centrifugal pumps

10. Remote acoustic analysis for tool condition monitoring

11. A low engery FPGA platform for real-time event-based control

12. Several Approaches for Anomaly Detection From Sound

13. An FPGA Platform Proposal for Real-Time Acoustic Event Detection

14. FPGA Implementations of Support Vector Machine Using Ising Model for AI on Things

15. FPGA-Embedded Anomaly Detection System for Milling Process

16. A machine sound monitoring for predictive maintenance focusing on very low frequency band

17. Design and Implementation of Acoustic Sensing System for Online Early Fault Detection in Industrial Fans

18. FPGA based monitoring platform for condition monitoring in cylindrical grinding

19. The development of surface acoustic wave sensors (SAWs) for process monitoring

20. One class svm for [link](https://www.researchgate.net/publication/265946573_One-Class_SVM_Based_Approach_for_Detecting_Anomalous_Audio_Events)

21. Anomalous Sound Detection [link](https://arxiv.org/pdf/2102.07820v1.pdf)

22. Discussion of Features for Acoustic Anomaly [link](https://www.researchgate.net/publication/365081524_Discussion_of_Features_for_Acoustic_Anomaly_Detection_under_Industrial_Disturbing_Noise_in_an_End-of-Line_Test_of_Geared_Motors)


<a id="orgad223be"></a>

### Potential Data Sets

1.  MIMII Dataset: Sound Dataset for Malfunctioning Industrial Machine Investigation and Inspection

2.  ToyADMOS dataset

3.  ToyADMOS dataset 2

4.  PRONOSTIA Bearing Dataset


<a id="orgab4afd0"></a>

### Existing Kaggle, Jupyter Notebooks, GitHub Repo's

1.  DCASE2020 Challenge Task 2 baseline variants     :KAGGLE:

2.  Federated Learning for Autoencoder-based Anomaly Detection in the Industrial Iot     :GITHUB:

3.  Self-Supervised Acoustic Anomaly Detection&#x2026;     :GITHUB:

    <https://github.com/Armanfard-Lab/AADCL>

4.  Unsupervised Anomaly Detection&#x2026;

    <https://www.kaggle.com/code/victorambonati/unsupervised-anomaly-detection>


<a id="orgf16e6fd"></a>

### Commercial, Industry Links:

1.  Webinar: Automated Acoustic&#x2026;

    <https://www.youtube.com/watch?v=-6B_XsEN2Q4>

2.  YT: One class SVM detection&#x2026;

    <https://www.youtube.com/watch?v=0dngOGhv5Mc>

3.  MSFT: Hybrid Model Approach for Real-Time Acoustic Anomaly Detection using Time-Series

4.  INTEL: Intel Labs uses AI and Audio Anomaly Detection to Prevent Semiconductor Manufacturing Malfunctions

5.  UE SYSTEMS INC: Ultra-Trak 750 ultrasonic amplitude sensor

6.  GFAI-TECH: 2D Outdoor Measurement, Acoustic Cameras

7.  NATIONAL THERMAL POWER CORPORATION: Ultrasonic, A new method for condition monitoring

8.  NASA: Preferred practice for Design & Test / Acoustic Noise (flight data microphones)

9.  SICK SENSOR INTELLIGENCE: Real-Time Condition Monitoring Sensor For Industrial Machinery (new MPB10 multiphysics sensor)

10. MRO MAGAZINE: Complete List of Condition Monitoring Techniques

11. PCB PIEZOELECTRONICS (AMPHENOL): Microphones for Aerospace/Acoustic Applications

12. ARTISS-MARPOSS: Acoustic Emission Sensors (AE-C & AE-C micro)

13. IBM / USPTO Patent: ACOUSTICS BASED ANOMALY DETECTION IN MACHINE ROOMS (date:2018-02-13, patent no:9,892,744)


<a id="orgd5b550e"></a>

## INSTRUCTOR QUESTIONS


<a id="org48c3346"></a>

### TODO 

