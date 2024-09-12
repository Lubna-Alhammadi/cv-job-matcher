# cv-job-matcher
# CV Job Matcher

This project uses semantic similarity to match a given CV to job descriptions from a predefined dataset. It provides the top 3 job descriptions that closely match the CV based on cosine similarity. The project uses Gradio for a web interface, and various NLP and machine learning libraries for processing.

## Requirements

- gradio
- pandas
- matplotlib
- transformers
- sentence-transformers
- langdetect
- torch

## Usage

Run the `app.py` script to launch the Gradio interface. Enter your CV text in the provided textbox, and the system will display the top 3 job descriptions that best match your CV.

## Installation

To install the required packages, use the following command:

```bash
pip install -r requirements.txt
