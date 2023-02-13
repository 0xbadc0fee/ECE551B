
# Table of Contents

1.  [Title <code>[1/1]</code>](#org396ab91)
2.  [Abstract <code>[1/1]</code>](#orge2fe704)
3.  [Index Terms <code>[1/1]</code>](#org7256c09)
4.  [Introduction <code>[6/6]</code>](#orgd7aea87)
5.  [Background <code>[3/3]</code>](#org5e6c6f7)
6.  [Methods & Materials <code>[0/0]</code>](#orgf99fe35)
    1.  [General ML Workflow <code>[0/3]</code>](#org0a50174)
    2.  [Specific ML Workflow <code>[0/3]</code>](#orge5b65bf)
    3.  [Specific Analysis Methods <code>[0/4]</code>](#org5f8c578)
7.  [Results](#org54c6fd3)
8.  [Discussion](#org79fef15)
9.  [Conclusion](#org7e8d8e8)
10. [Appendix](#orgb7c8a82)
11. [Bibliography](#org7370d14)



<a id="org396ab91"></a>

# Title <code>[1/1]</code>

-   [X] Content

    A proposed automatic in-situ acoustic anomaly detection method for the condition monitoring of remote vertical turbine pump stations


<a id="orge2fe704"></a>

# Abstract <code>[1/1]</code>

-   [X] Content

    The condition monitoring of vertical turbine pump stations, found on large irrigation systems in remote areas presents a number of challenges that make it well suited for emerging techniques in the fields of machine learning, embedded systems, and machine condition monitoring.  Such pump stations employ arrays individual vertical turbine pumps, capable of individual or combined operation, are often remotely located, remotely controlled, serve mission critical roles to both private and public interests, and are very costly to repair in both time and labor.  Further, besides high repair costs due to machine break downs, even more financially costly are small degradations of efficiency in otherwise normal operation.  Unchecked, such variations represent tens of thousands of dollars in avoidable losses.  Given access to real-time, remotely accessible, and relatively accurate machine condition monitoring data; operators could both schedule predictive maintenance as well as factor in relative pump to pump efficiencies when responding for variable water demand down stream of the pump station.
    
    As almost all such systems are operated via programmable-logic-controllers, most such systems already have some degree of condition monitoring feedback built into them.  Most commonly found are feedback inputs reflecting amperage draw, frequency, voltage, temperature, rpm, and in some cases fluid flow.  The size and remoteness of these systems makes many common machine condition monitoring methods unfeasible.  Methods such as vibration analysis,
    
    What we propose here is an automatic system that can be installed near, but not interfere with, such pump stations, outside of the control loop, which can monitor for and report on operation anomalies through the detection of acoustic anomalies during station operation.


<a id="org7256c09"></a>

# Index Terms <code>[1/1]</code>

-   [X] Content

    Acoustic emission, Anomaly detection, Machine learning, Condition monitoring, Real-time, Signal Processing, Spectrogram, Acoustic signal processing, Embedded systems, 


<a id="orgd7aea87"></a>

# Introduction <code>[6/6]</code>

-   [X] **A:** Role of Irrigation

    Since the begining of recorded time, the life blood of any human civilization has always been linked to water.  Since long before the basin irrigation of Ancient Egypt or canal networks of the early Mesopotamians, there has been a continuous need to both improve existing and develop new technologies for transporting water.  Irrigation, the supply of water to land for the purpose of growing crops, has been an especially forceful driver of improvements and new innovations.  Almost all modern irrigation processes begin with the need to lift volumes of water from lower elevations to high elevations; whether for immediate use, reservoir storage, or to leverage gravity to build pressure.

-   [X] **B:** Modern Large Scale Irrigation

    Today much of that lifting work is done through the use of Vertical Turbine Pumps.  A vertical turbine pump is a type of centrifugal pump built to be submerged in water \cite{scherer1993irrigation}, are driven by direct mounted electric motors, and capable of lifting large volumes of water at greater efficiencies than traditional centrifugal pumps.  Vertical turbine pumps can be found in many different sizes and applications.  Because of their efficency, almost all large scale irrigation systems rely on vertical turbine pump technology.

-   [X] **C:** Vertical Turbine Pumps

    A single Vertical turbine pump consists of the following elements, typically found from bottom (input) to top (output): a suction filter or screen, a series of pump stages called the bowl assembly, the column assembly, and finally the head assembly.  Mounted atop the head assembly is an electric motor.  The motor is coupled to a drive shaft that extends the full length of the column and bowl assemblies.  This drive shaft turns the impellers housed inside the bowls of the bowl assemby.  The number of bowl assemblies varies depending on purpose and design of the system.  The electric motors atop the pumps are typically connected to a variable frequency drive, which is itself most often connect to a programmable logic controller.  A typical VFD & PLC installation will often provide a number of feedback parameters for use by the operators.  At a minimum, operators usually have visibility on amerage draw, voltage, line frequency, and motor rpm.  Depending on installation, additional monitoring parameters may include fluid flow, temperature measurements, and pressure readings.  Vertical turbine pumps can be run individually or in tandem within a large array of such pumps.

-   [X] **D:** Multi Unit Pump Stations

    A vertical turbine pump station represents a system in which multiple vertical turbine pumps are linked together.  These stations draw input water from the same source, and combine the outputs into a common manifold or reservoir depending on design.  During operation, depending on demand, the number of pumps engaged may range from all, to some, or even just one.  These pump stations are usually very large, remotely located, and quite loud when in full operation.  As crop growing cycles are inflexibly linked to annual cycles, and absence of water can permanently alter soil conditions not just reduce crop growth; uptime availability of these systems is considered extremely critical.  Standard operating procedures involve predictive maintenance and rebuilds of individual pumps during non-growing seasons.  Year to year, the operators of these systems will select a number of pumps to be removed and sent to machine shops that specialize in the teardown, inspection, repair, re-assembly, testing, and installation of such pumps.  The down time for a full rebuild is typically measured in months.  Even when scheduled in advance, the rebuild process is time consuming and costly.

-   [X] **E:** The Problem

    The problem this paper seeks to address is that the operators of such systems have limited information on the relative condition of their pumps, both individually and as systems.  As stated above, most of the typical feedback parameters come from the VFD's or the PLC's.  Feedback from these devices is typically found within the PLC control network itself.  Sometimes additional sensing devices such as flow meters, pressure transducers, and thermocouples are also incorporated.  The information provided by these auxiliary devices is typically segregated from the PLC control network.  The goal of this paper is to demonstrate a system that by continuosly observing sound emissions from such pump stations a properly trained machine learning algorithm could report and log acoustic anomalies that the operators could utilize in both planning maintenance as well as factor into regular operation procedures.

-   [X] **F:** Proposed Solution

    Detection and recognition are two different applications of machine learning often requiring different algorithms as well as specially labeled data sets.  They can though be built on shared archictecture if planned early on in the process.  Typically, detection is a binary classification where recognition is more often a multiclass classification.  An example of detection use in vertical pump stations would be logging whether sound current acoustic emissions are likely within expected ranges or outside of expected ranges.  Likewise, a possible recognition algorithm may attempt to classify detected anomalies as being within such categories as: cavitation, bearing wear, debri ingest, or other mechanical failure.


<a id="org5e6c6f7"></a>

# Background <code>[3/3]</code>

-   [X] General Overview MCM&#x2026;

    There are a number of modern approaches to machine condition monitoring.  In terms of machine condition monitoring, these pump stations represent a family of rotating machinery, that cannot be easily moved or disassembled, must be kept in production as much as possible, and are subject to harsh operating conditions.
    The minimum selection criteria for this project requires that any method used must be\newline
    
    \begin{enumerate}
    \item Non-destructive
    \item In-situ
    \item PLC safe
    \item Harsh environment
    \item Minimal installation effort \newline
    \end{enumerate}
    
    Based on that criteria some available technologies include vibration analysis, electrical performance analysis, hydraulic monitoring (flow, pressure, temperature), visual analysis, and acoustic analysis.  The oil and gas industry has developed a number of ultrasonic technologies that can be used to identify the location and propogation of cracks in piping.  The power transmission industry has developed a number of both vibration based and tribology (oil analysis) based methods for monitoring rotating machinery.  Also the aerospace industry has contributed a number of technologies in acoustic sensing such as special microphones used on aircraft during flight testing or in wind-tunnel tests.

-   [X] Specific MCM methods for this case&#x2026;
    -   Non-destructive
    -   In-situ
    -   PLC safe
    -   Harsh Environment
    -   Minimima install footprint
-   [X] Justify Acoustic Approach / Selection


<a id="orgf99fe35"></a>

# Methods & Materials <code>[0/0]</code>

-   <https://cloud.google.com/ai-platform/docs/ml-solutions-overview>
-   <https://ml-ops.org/content/end-to-end-ml-workflow#:~:text=The%20core%20of%20the%20ML,to%20train%20an%20ML%20model>.
-   <https://www.datacamp.com/blog/a-beginner-s-guide-to-the-machine-learning-workflow>
-   <https://cms.tinyml.org/wp-content/uploads/talks2020/tinyML_Talks_Ian_Campbell_201208.pdf>
-   <https://www.mdpi.com/2079-9292/10/19/2329>


<a id="org0a50174"></a>

## General ML Workflow <code>[0/3]</code>

-   [ ] Data Engineering

    [GENERAL DATA CONTENT]

-   [ ] Model Engineering

    [GENERAL MODEL CONTENT]

-   [ ] Model Deployment

    [GENERAL DEPLOY CONTENT]


<a id="orge5b65bf"></a>

## Specific ML Workflow <code>[0/3]</code>

-   [ ] **Data:** Specific Methods
    -   [ ] **Hardware:** Signal Capture
        -   [ ] choose transducer (microphone(s))
        -   [ ] choose recording hardware (multi channel, SoC, small device, &#x2026;)
        -   [ ] mounting?
        -   [ ] power supply?
        -   [ ] networking?
    -   [ ] **Software:** Signal Manipulation
        -   [ ] Signal storage?
        -   [ ] Signal conditioning? (trimming, cleaning, filtering)
        -   [ ] Signal conversion? (convert audio to graphical spectrograms, circular plots?)

    [SPECIFIC DATA METHODS CONTENT]

-   [ ] **Model:** Specific Methods
    -   [ ] Algorithm&#x2026;

    [SPECIFIC MODEL METHODS CONTENT]

-   [ ] **Deployment:** Specific Methods
    -   [ ] **HMI:** End user interaction&#x2026;

    [SPECIFIC DEPLOY METHODS CONTENT]


<a id="org5f8c578"></a>

## Specific Analysis Methods <code>[0/4]</code>

-   [ ] Discuss Pass / Fail threshold (acceptable false alarms rate)
-   [ ] Discuss Metrics (AUC, ROC, Confusion Matrix, etc)
-   [ ] Discuss Trial & Error, Iterations,
-   [ ] Discuss End User Interaction, HMI ?


<a id="org54c6fd3"></a>

# Results


<a id="org79fef15"></a>

# Discussion


<a id="org7e8d8e8"></a>

# Conclusion


<a id="orgb7c8a82"></a>

# Appendix


<a id="org7370d14"></a>

# Bibliography

