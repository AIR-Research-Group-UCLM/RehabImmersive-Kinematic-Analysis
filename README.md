# RehabImmersive-Kinematic-Analysis

**A unified software ecosystem for upper-limb neurorehabilitation.**
Combines VR serious games (Meta Quest) for motion capture with a privacy-focused web tool for kinematic analysis.

---

## 🎯 Abstract

This repository hosts the source code and software artifacts for the **Rehab-Immersive** system, a comprehensive solution designed to bridge the gap between Immersive Virtual Reality (IVR) therapy and objective clinical assessment.

The system addresses two critical barriers in neurorehabilitation:
1.  **Acquisition:** Providing accessible, controller-free serious games that capture high-precision 6DoF motion data using consumer hardware (Meta Quest).
2.  **Analysis:** Democratizing kinematic assessment via a "local-first" web tool that automatically calculates validated clinical metrics—such as **ROM Volume**, **Tortuosity (Efficiency)**, and **Movement Smoothness (NVP)**—without requiring engineering expertise or cloud dependencies.

## 📋 Table of Contents

1. [Overview](#-overview)
2. [Repository Structure](#-repository-structure)
3. [Software Components](#-software-components)
    - [VR Acquisition (Serious Games)](#1-vr-acquisition-serious-games)
    - [Web Analysis Tool](#2-kinematic-analysis-web-tool)
4. [Data Format](#-data-format)
5. [Installation & Usage](#-installation--usage)
6. [Citation](#-citation)
7. [License & Acknowledgments](#-license--acknowledgments)

## 🔭 Overview

The ecosystem is composed of two independent but complementary modules:

* **VR Acquisition Module:** A set of serious games (Virtual Box & Block Test and Adapted Handball) running on Meta Quest devices. These applications act as the "sensor," logging biomechanical data at 72/90 Hz.
* **Analysis Module:** A browser-based dashboard that ingests the raw CSV telemetry from the headset and generates interactive 3D visualizations and quantitative clinical reports.

## 📁 Repository Structure

```text
RehabImmersive-Kinematic-Analysis/
├── 📂 Serious_Games_VR_apks/    # Standalone Android packages for Meta Quest
│   ├── RehabImmersive_BBT.apk       # Virtual Box & Block Test (Unimanual)
│   └── RehabImmersive_Handball.apk  # Adapted Handball Game (Bimanual)
│
├── 📂 Kinematic_analysis/       # The Web-Based Analysis Tool
│   ├── index.html                   # Main entry point (Dashboard)
│   ├── css/                         # Stylesheets
│   └── js/                          # Logic (Parsing, Metrics, Plotly/Chart.js)
│
├── 📂 CSV_Examples/             # Sample datasets for testing
│   ├── BBT_Healthy_Sample.csv       # Sample telemetry from vBBT
│   └── Handball_Patient_Sample.csv  # Sample telemetry from Handball
│
├── LICENSE                      # MIT License
└── README.md                    # Project Documentation
