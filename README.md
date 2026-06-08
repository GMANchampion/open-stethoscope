# open-stethoscope
Overview: Open-source adaptive digital stethoscope with real-time noise cancellation, acoustic biomarker logging, and reproducible hardware/software files for low-cost cardiopulmonary auscultation research. 

The Problem: Auscultation (listening to heart and lung sounds with a stethoscope) is one of the most widely used diagnostic tools in medicine. But, the widespread acoustic stethoscope has changed almost nothing since 1816, and is subjective, non-recordable, dependent on clinician experience, and performs poorly in noisy environments. These limitations become critical in low-resource settings, where the gap in accessible respiratory diagnostics is widest.

Why it Matters: Asthma affects over 300 million people globally. COPD (chronic obstructive pulmonary disease) is the third leading cause of death worldwide. Pneumonia kills over 2 million children under five annually, and most of them live in settings where a pulmonologist and a quiet examination room are both unavailable. Digital stethoscopes offer a path forward, but the cheapest validated commercial options start at $200–$500.

Thesis: We design, build, and openly publish a sub-$100 digital stethoscope (containing an Arduino Nano + MEMS microphone + 3D-printed chest piece) with onboard adaptive noise filtering and a Raspberry Pi logging hub. We rigorously characterize its acoustic performance across four controlled noise environments (anechoic, clinic-level, ICU-analog, domestic) and compare it in parallel against a Littmann 3200 (the markets leading electronic stethoscope) — to produce the first openly reproducible stethoscope characterization dataset and establishing a validated open-hardware reference design for low-resource auscultation research.

Timeline: 
Phase 1 (June 8 – June 28) - Hardware Build: 3D print chest piece · Wire MEMS mic to Arduino Nano · Connect Raspberry Pi · Wire piezoelectric sensor · Basic audio capture test
Phase 2 (June 29 – July 19) - Signal Processing: Bandpass filter (20–1000 Hz) · Adaptive noise subtraction (LMS filter) · Real-time FFT on Arduino · Build Python logging pipeline · Unit-test filter on recorded clips
Phase 3 (July 20 – Sept 6) - Data Collection: Build chest phantom · Record in 4 noise environments · Simultaneous Littmann 3200 comparison · ≥200 paired recordings · Label dataset with metadata CSV
Phase 4 (Sept 7 – Oct 5) - Analysis & Write-Up: Statistical analysis (SNR, Cohen's κ, ANOVA) · Open-source all files on GitHub + Zenodo · Write HardwareX manuscript · Internal review & revise · Submit by October 5

Repository Structure:

Hardware List: 
- 3D-printed chest piece files
- Enclosure CAD files
- KiCad schematics
- Wiring diagrams
- Bill of materials
- Assembly photos
- Calibration notes

Target Journal (HardwareX): 
