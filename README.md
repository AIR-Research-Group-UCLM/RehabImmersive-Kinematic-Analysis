# RehabImmersive-Kinematic-Analysis

A lightweight, local-first kinematic acquisition and analysis module within the broader **Rehab-Immersive** platform.  
It provides **controller-free VR serious games** (Meta Quest) to log **6DoF head and hand kinematics**, plus a **standalone browser-based tool** to compute and visualize kinematic indicators for **unimanual** and **bimanual** upper-limb exercises.

## Description

This repository accompanies the SoftwareX manuscript describing a unified workflow that connects immersive VR-based occupational therapy tasks with objective kinematic assessment. The workflow is designed to be practical in real settings by avoiding external motion-capture infrastructures, minimizing operational complexity, and keeping processing local by default.

The module includes:
1. **VR acquisition (Meta Quest APKs)** implementing two serious-game tasks and local telemetry logging.
2. **A standalone browser-based analysis suite** that parses CSV logs, computes kinematic indicators, and provides interactive visualizations to support clinical interpretation.

## Key features

- **Local-first workflow**: analysis runs entirely in the browser by default (no cloud, no external servers).
- **Controller-free interaction**: designed for users with limited grasp capacity (hand tracking).
- **Mono- and bimanual analysis**: supports unimanual dexterity and bimanual coordination sessions.
- **Automated metrics and interactive plots**, including:
  - velocity profiles,
  - smoothness (Number of Velocity Peaks, NVP),
  - path efficiency (tortuosity),
  - functional ROM volume,
  - head–hand relationship measures (compensation proxy),
  - left vs. right comparative reporting.


## Repository structure

├── CSV_Examples
│   ├── BBT_1.csv
│   ├── BBT_2.csv
│   ├── HANDBALL_2_2_1_11_26_2025.csv
│   └── HANDBALL_3_2_1_11_26_2025.csv
├── Kinematic_analysis
│   └── rehab_kinematic_analysis.html
├── LICENSE
├── README.md
└── Serious_Games_VR_apks
    ├── BBT_v_2_3.apk
    └── hbt_v_2_2.apk

---
## Running the VR applications (Meta Quest)

### Prerequisites
- Meta Quest 2 or Meta Quest 3
- Developer Mode enabled
- An installation method such as:
  - **Meta Quest Developer Hub (MQDH)**, or
  - `adb` (Android Platform Tools)

### Install APKs
- vBBT: `Serious_Games_VR_apks/BBT_v_2_3.apk`
- Handball: `Serious_Games_VR_apks/hbt_v_2_2.apk`

You can install using MQDH or via `adb install <apk>`.

### Retrieve the generated CSV logs
After playing, the applications store the kinematic logs locally on the headset.  
To retrieve them, use MQDH (File Manager) or `adb pull` to copy the generated `.csv` files to your computer.


## Quick start (no installation)

### 1) Run the analysis tool locally
1. Open: `Kinematic_analysis/rehab_kinematic_analysis.html` in a modern desktop browser.
2. Choose the analysis mode (**Unimanual** / **Bimanual**).
3. Drag and drop one of the example CSV files from `CSV_Examples/`.

This reproduces the full analysis workflow (metrics and plots) without installing anything.

---

## How to analyze your own recordings

1. Copy the CSV logs from the headset to your computer.
2. Open `Kinematic_analysis/rehab_kinematic_analysis.html`.
3. Select:
   - **Unimanual** for vBBT sessions, or
   - **Bimanual** for Handball sessions.
4. Upload the CSV.
5. Use:
   - the **ROI controls** to exclude calibration or rest frames,
   - the **playback** to relate peaks to movement phases,
   - the plots to inspect 2D/3D trajectories and time evolution.

---

## Citation

If you use this repository in academic work, please cite:
1. The SoftwareX paper describing this kinematic module/pipeline (to be added once published).
2. The Rehab-Immersive framework paper:

**Reference (framework paper):**  
Herrera, V., Vallejo, D., Castro-Schez, J. J., Monekosso, D. N., de los Reyes, A., Glez-Morcillo, C., and Albusac, J. (2023). *Rehab-Immersive: A framework to support the development of virtual reality applications in upper limb rehabilitation*. **SoftwareX**, 23, 101412. https://doi.org/10.1016/j.softx.2023.101412


## License

This project is released under the **MIT License**. See `LICENSE`.

## Contributors / Contact

- **Javier Albusac** (corresponding author): javieralonso.albusac@uclm.es  
- **Vanesa Herrera**  
- **David Vallejo** 
- **Ana de los Reyes Guzmán**
- **Carlos González Morcillo**

## Acknowledgments

This work has been conducted within the scope of the Spanish national research project **Rehab-Immersive** and has been supported by the Spanish Ministry of Science, Innovation and Universities under grants **PID2020-117361RB-C21** and **PID2020-117361RB-C22**. The authors also acknowledge the collaboration of the **National Hospital for Paraplegics (Toledo, Spain)**, in particular the **Biomechanics and Technical Aids Unit**, for their clinical guidance and o
::contentReference[oaicite:0]{index=0}
