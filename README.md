# open-stethoscope
## **Overview**: 
Open-source adaptive digital stethoscope with real-time noise cancellation, acoustic biomarker logging, and reproducible hardware/software files for low-cost cardiopulmonary auscultation research. 

## **The Problem**: 
Unlike nearly every other diagnostic tool, Auscultation (listening to heart and lung sounds with a stethoscope) remains one of the most widely used diagnostic tools in medicine. Despite this, the widespread acoustic stethoscope has barely changed since 1816. Moreover, it is subjective and non-recordable, while being dependent on the clinician's experience and performing poorly in noisy environments. In low-resource settings where there is a large gap in accessible respiratory diagnostics, these become highly critical limitations.

## **Why it Matters**: 
Asthma affects over 300 million people globally, COPD (chronic obstructive pulmonary disease) is the third leading cause of death worldwide, and Pneumonia kills over 2 million children under five annually, with most of them living in settings where a pulmonologist and a quiet examination room are both unavailable. While there are valid commercial options, most of them start at around $200-$500, making them unaffordable to many.

## **Thesis:** 
We design, build, and openly publish a sub-$100 digital stethoscope (containing an Arduino Nano + MEMS microphone + 3D-printed chest piece) with onboard adaptive noise filtering and a Raspberry Pi logging hub. We rigorously characterize its acoustic performance across four controlled noise environments (anechoic, clinic-level, ICU-analog, domestic) and compare it in parallel against a Littmann 3200. (the markets leading electronic stethoscope). The goal is to produce the first openly reproducible stethoscope characterization dataset and establishing a validated open-hardware reference design for low-resource auscultation research.

## **Timeline:** 
**Phase 1 (June 8 – June 28) -** Hardware Build: 3D print chest piece · Wire MEMS mic to Arduino Nano · Connect Raspberry Pi · Wire piezoelectric sensor · Basic audio capture test

**Phase 2 (June 29 – July 19) -** Signal Processing: Bandpass filter (20–1000 Hz) · Adaptive noise subtraction (LMS filter) · Real-time FFT on Arduino · Build Python logging pipeline · Unit-test filter on recorded clips

**Phase 3 (July 20 – Sept 6) -** Data Collection: Build chest phantom · Record in 4 noise environments · Simultaneous Littmann 3200 comparison · ≥200 paired recordings · Label dataset with metadata CSV

**Phase 4 (Sept 7 – Oct 5) -** Analysis & Write-Up: Statistical analysis (SNR, Cohen's κ, ANOVA) · Open-source all files on GitHub + Zenodo · Write HardwareX manuscript · Internal review & revise · Submit by October 5

## **Repository Structure:**
**Analysis**: Python analysis scripts for the Open Stethoscope project. 
  **Purpose**: This folder will contain code for processing recordings, calculating acoustic metrics, generating figures, and reproducing the results. 

**Data Dataset**: Documentation for the Open Stethoscope project. 
  **Purpose**: This folder will document the recorded metadata, dataset structure, labeling conventions, and links to released data. 

**Docs**: Project documentation for the Open Stethoscope project. 
  **Purpose**: This folder will contain research notes, build instructions, protocols, manuscript drafts, and supplementary documentation. 

**Firmware**: Arduino firmware for the Open Stethoscope project. 
  **Purpose**: This folder will contain documentation on all electronic firmware components

**Hardware**: Hardware design files for the Open Stethoscope project. 
  **Purpose**: This folder will contain CAD files, schematics, enclosure designs, chest piece models, wiring diagrams, and the bill of materials. 

## **Hardware List:** 
- 3D-printed chest piece files
- Enclosure CAD files
- KiCad schematics
- Wiring diagrams
- Bill of materials
- Assembly photos
- Calibration notes

## **Target Journal (HardwareX):** 
**What is it?:** HardwareX is an open-access and peer-reviewed journal that is centered around open-source scientific hardware, meaning that anyone can access them. Researchers publish designs for lab equipment, sensors, 3D-printed tools, educational devices, and other scientific instruments. This allows others to build, modify, and improve these submissions.

**Why HardwareX?:** HardwareX’s purpose directly aligns with the objective of this type of project. There is no institutional affiliation required, and their stated scope explicitly covers 'low-cost alternatives to existing tools' and 'wearable/out-of-lab sensors,' exactly what this project aims to do.
