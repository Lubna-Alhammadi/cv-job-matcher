##CV to Job Description Matching Project
#Purpose of the Project
This project aims to help job seekers by matching their CVs to job descriptions from major companies using semantic similarity. By analyzing the text content of the CV, the system identifies and presents the top three job descriptions that best match the provided CV. Additionally, it provides translations for CVs that are not in English, as well as the corresponding job descriptions.

Main Files and Their Functions
Project.ipynb: This is the primary script that runs the project. It includes the following functionalities:

Contains predefined job descriptions from major companies like Google, Amazon, Microsoft, etc.
Detects the language of the input CV.
Translates the CV to English if necessary using Hugging Face’s translation pipeline.
Compares the CV with the job descriptions using semantic similarity through SentenceTransformer.
Outputs the top 3 matching job descriptions and their similarity scores in a bar chart.
Translates job descriptions to the CV’s original language if the input CV is not in English.
Pipeline.ipynb: This Python notebook demonstrates how the Hugging Face text-to-text pipeline works independently, without the Gradio interface. It walks through using Hugging Face’s translation and semantic similarity tools with hardcoded inputs.

Gradio.ipynb: This notebook shows how Gradio components work using hardcoded data. It demonstrates the basic setup of a Gradio interface with similar functionalities, but without relying on external inputs or complex workflows.

Models
Semantic Similarity Model
The project uses the SentenceTransformer model, specifically the sentence-transformers/all-MiniLM-L6-v2, to compute semantic similarity between the CV and job descriptions. The model works by converting both the CV and job descriptions into embeddings (vector representations of the text). It then calculates the cosine similarity between these embeddings to determine how closely the texts match in meaning. The higher the cosine similarity score, the more similar the texts are. This allows the system to rank the job descriptions and find the top 3 that best match the content of the provided CV.

Translation Model
The project also uses the Hugging Face pipeline for language translation. The model used for translation is facebook/nllb-200-distilled-600M, a multilingual model capable of translating texts between multiple languages. The language of the input CV is detected using the langdetect library. If the CV is not in English, it is translated to English before performing semantic similarity comparison. Additionally, if the job descriptions need to be displayed in the CV's original language (if not in English), the model can translate them back to that language, ensuring the user sees relevant job descriptions in their native language.

Expected Output from the Gradio Interface
Job Summaries: The top 3 job descriptions that match the provided CV will be displayed, either in English or translated into the CV's original language.
Top 3 Matching Job Descriptions Plot: A bar chart displaying the similarity scores of the top 3 matched job descriptions will be shown.
Running Hugging Face Project Page
You can access the project running on Hugging Face Spaces here: Hugging Face CV Job Matcher.

Video Walkthrough of the Python Notebook
An uploaded video walkthrough of the Python notebook explaining the project step-by-step is available. You can view the video by clicking the following link:

Click here to Watch the video walkthrough
