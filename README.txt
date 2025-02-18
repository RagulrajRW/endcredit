# Video Processing Flask Application

## Overview

This is a Flask-based web application that processes uploaded videos by extracting frames, performing Optical Character Recognition (OCR) on them to extract text, and identifying names using Natural Language Processing (NLP). The extracted names are then compared against a reference name list to find common matches, which are saved in a CSV file.

## Features

- Upload a video file via a web interface.
- Extract frames from the video at 1-second intervals.
- Perform OCR on extracted frames using Tesseract.
- Identify names from the extracted text using SpaCy's NLP model.
- Compare extracted names against a reference name list.
- Generate a CSV file with common names found.
- Provide a downloadable link for the processed CSV file.

## Technologies Used

- **Flask**: Web framework for handling video uploads and processing requests.
- **OpenCV (cv2)**: Image processing for OCR.
- **Pytesseract**: OCR tool to extract text from images.
- **SpaCy**: NLP model for extracting named entities.
- **FFmpeg**: Extracts frames from the uploaded video.
- **CSV**: Stores and compares extracted names.
- **HTML/CSS/JavaScript**: (Optional) for frontend development.

## Prerequisites

Before running this application, ensure you have the following installed:

1. Python (>= 3.7)
2. FFmpeg (for frame extraction)
3. OpenCV (`cv2`)
4. Tesseract OCR
5. Flask
6. SpaCy with `en_core_web_trf` model
7. Required Python libraries:

```bash
pip install flask opencv-python pytesseract spacy
```

## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-repo-name.git
cd your-repo-name
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Download the SpaCy model:

```bash
python -m spacy download en_core_web_trf
```

4. Ensure FFmpeg is installed and added to your system's PATH.
5. Configure Tesseract OCR by installing it from [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) and ensuring it is accessible from the command line.

## Directory Structure

```
project_root/
│── uploads/      # Stores uploaded video files
│── frames/       # Stores extracted frames
│── outputs/      # Stores extracted and matched names
│── app.py        # Flask application
│── requirements.txt  # Python dependencies
│── index.html    # Frontend file (optional)
```

## Running the Application

Run the Flask server:

```bash
python app.py
```

This will start a local server on `http://127.0.0.1:5000/`.

## Usage

1. Open the web interface in a browser.
2. Upload a video file.
3. The application extracts frames and performs OCR and NLP to extract names.
4. The extracted names are compared against a reference list.
5. A CSV file containing common names is generated and available for download.
6.

## Troubleshooting

- **FFmpeg error**: Ensure FFmpeg is installed and accessible from the command line.
- **Tesseract OCR error**: Set the correct path for Tesseract OCR if it's not found.
- **Missing dependencies**: Run `pip install -r requirements.txt` to install required packages.

## License

This project is open-source and available under the MIT License.

