# Experiment Management Application

## Overview
The **Experiment Management Application** is a Python-based graphical user interface (GUI) designed to manage and analyze emotion-related experiments using data from iMotions. This application integrates the efforts of multiple contributors, each focusing on different data modalities:

- **Web Emotion Analysis**: Analyze user interactions on websites to generate heatmaps based on emotional and gaze data.
- **Image Emotion Analysis**: Process images to analyze emotions using computer vision techniques.
- **Video Emotion Analysis**: Evaluate videos for emotion detection using advanced processing.

This repository serves as a cohesive platform for conducting and visualizing these experiments, showcasing how different emotion analysis approaches can generate insights.

---

## Key Features

- **Integrated GUI**:
  - Unified interface to manage web, image, and video-based experiments.
  - Easy-to-use file selection, processing, and visualization tools.

- **Web Emotion Analysis**:
  - Processes web interaction data (mouse activity, scroll position, gaze tracking).
  - Generates heatmaps over web page screenshots to visualize user focus and emotions.

- **Image Emotion Analysis**:
  - Extracts emotions from static images using machine learning models.

- **Video Emotion Analysis**:
  - Analyzes video content to identify and quantify emotions over time.

---

## Project Structure

```bash
.
├── LICENSE
├── README.md
├── app.py
├── emotiongsr
│   ├── __init__.py
│   └── dataprocessor.py
├── images_app.py
├── multimotions
│   └── dataprocessor.py
├── requirements.txt
├── sample_data
│   ├── CleanedData
│   ├── Data
│   ├── Images
│   └── WebData
├── videos_app.py
└── websites_app.py
```

---

## How It Works

### Web Emotion Analysis
1. **Input**: 
   - CSV file containing web interaction data.
   - CSV file with iMotions data.
   - Screenshot of the web page.
2. **Processing**: 
   - Synchronizes web and iMotions data using timestamps.
   - Computes gaze coordinates and emotional metrics.
   - Generates heatmaps overlayed on web screenshots.
3. **Output**:
   - Heatmap visualization saved as a high-resolution image.

### Image Emotion Analysis
1. **Input**:
   - One or more images for analysis.
2. **Processing**:
   - Extracts facial features.
   - Computes emotion scores (e.g., joy, anger, sadness).
3. **Output**:
   - Annotated images with emotion metrics.

### Video Emotion Analysis
1. **Input**:
   - Video files.
2. **Processing**:
   - Processes frames to detect faces and emotions.
   - Generates a time-series visualization of emotion trends.
3. **Output**:
   - Time-series data and visualizations for emotion dynamics.

---

## Requirements

### Prerequisites
- Python 3.8 or above
- Required libraries: `numpy`, `pandas`, `matplotlib`, `tkinter`, `Pillow`, `scipy`

### Installation
Clone this repository and install dependencies:
```bash
git clone <repository_url>
cd <repository_name>
pip install -r requirements.txt
```

---

## Usage

### Running the Application
To start the Experiment Management Application, run:
```bash
python app.py
```

### Navigating the GUI
1. Select an experiment type:
   - Website
   - Image
   - Video
2. Follow the prompts to upload necessary files.
3. Process data and view or save visualizations.

---

## Authors

- **Lesly C Guerrero Velez**
- **Manuel J Romero Olvera**
- **Mohammad, Priyank, Sajeda** (Module Contributions)

---

## License
This project is licensed under the [MIT License](LICENSE).

For further questions or contributions, please create an issue or pull request in this repository.
