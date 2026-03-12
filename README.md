# Intelligent Document Processing Pipeline

This project implements a complete Intelligent Document Processing (IDP) pipeline that processes document images, extracts text, classifies documents, and generates summarized and translated outputs.

The system combines Computer Vision, OCR, Deep Learning, Fuzzy Logic, and NLP models to automatically analyze and understand document images.

Features

The pipeline performs the following tasks:

Image Preprocessing

Reads document images

Applies rotation correction

Enhances images for OCR

CNN Document Classification

Classifies document images into predefined classes

Uses convolutional neural networks for feature extraction

OCR Text Extraction

Extracts text from document images

Converts extracted text into structured format (CSV)

Orientation Detection

Detects whether a document image is rotated

Suggests required rotation angle

LSTM Text Classification

Performs document classification based on extracted text

Uses bidirectional LSTM architecture

Fuzzy Logic Classification

Combines multiple signals to improve classification reliability

Document Summarization

Generates concise summaries of extracted document text

Uses transformer-based NLP models

Document Translation

Translates extracted text into different languages

Complete IDP Pipeline

Integrates all modules into a single automated workflow

Project Architecture

Document Image
      │
      ▼
Image Preprocessing
      │
      ▼
CNN Image Classification
      │
      ▼
OCR Text Extraction
      │
      ▼
LSTM Text Classification
      │
      ▼
Fuzzy Classification
      │
      ▼
Text Summarization
      │
      ▼
Text Translation
      │
      ▼
Final Structured Output

Installation

Run the following commands once to install dependencies.

pip install opencv-python Pillow
pip install scipy scikit-fuzzy networkx
pip install pytesseract pdf2image
pip install transformers[torch]
pip install accelerate
pip install tiktoken
pip install sentencepiece
pip install protobuf
pip install numpy<2.0.0
pip install --upgrade ipywidgets
Required Libraries

The project uses the following key libraries:
PyTorch
OpenCV
NumPy
Pandas
Scikit-learn
Tesseract OCR
Transformers (HuggingFace)
Scikit-Fuzzy
PDF2Image
PIL (Pillow)

Dataset
The dataset consists of document images stored in directories representing different classes.
Example structure:

dataset/
│
├── invoice/
├── letter/
├── form/
├── receipt/
└── memo/

Each folder contains document images belonging to that class.

Model Components

CNN Module
Performs image-based document classification
Uses convolutional layers for feature extraction.

OCR Module
Uses Tesseract OCR to extract text from images.

LSTM Module
Processes extracted text
Performs text-based classification

Fuzzy Classification
Combines outputs from CNN and LSTM models
Improves classification reliability.

Summarization Module
Uses transformer-based summarization models to generate document summaries.

Translation Module
Translates document text into selected languages.

Running the Pipeline

Run the notebook step-by-step:

Install dependencies
Load dataset
Train CNN model
Perform OCR
Train LSTM text classifier
Run fuzzy classification
Generate summaries
Translate output text
Execute the final IDP pipeline


The final output includes:

Document class
Extracted text
Orientation correction
Text summary
Translated text

