# Resume Parser

A resume parser that extracts relevant details such as contact information, skills, education, and work experience from resumes in PDF and DOCX formats. This tool uses natural language processing (NLP) and regular expressions to preprocess and extract information.

## Features

- Extracts text from PDF and DOCX files.
- Preprocesses text to remove unwanted characters and normalize content.
- Extracts contact information including phone numbers and email addresses.
- Identifies and extracts skills, education, and work experience sections from resumes.
- Utilizes Flask for a web interface to upload and process resumes.
- Deploys the application using ngrok for public URL access.

### Install Dependencies

pip install -r requirements.txt

### Download NLTK Data

import nltk

nltk.download("punkt")

nltk.download("stopwords")

### Install and Configure ngrok

pip install pyngrok

ngrok authtoken YOUR_NGROK_AUTH_TOKEN

## Usage

### Run the Parser

Navigate to the directory containing the resume files and update the path in the script. Run the script to extract and preprocess the data.

### Extract Data

The extracted data is saved in a CSV file in the specified directory.

### Start the Flask Application

python app.py

This will start the Flask server and provide a public URL via ngrok.

### Upload and Process Resumes

Access the application through the provided ngrok URL, upload resumes, and view the extracted details.

## Project Structure

- **data**: Directory containing resume files for processing.
- **templates**: HTML templates for the Flask web interface.
- **static**: Static files for the web interface (CSS, JS).
- **app.py**: Main Flask application script.
- **requirements.txt**: List of required Python libraries.

## Functions Overview

### Text Extraction Functions

- **extract_text_from_pdf**: Extracts text from PDF files.
- **extract_text_from_doc**: Extracts text from DOCX files.

### Text Preprocessing Functions

- **preprocess**: Preprocesses text by converting to lowercase, removing special characters, and tokenizing.

### Contact Information Extraction Functions

- **extract_phone_numbers**: Extracts phone numbers from text.
- **extract_email_addresses**: Extracts email addresses from text.

### Section Extraction Functions

- **extract_skills**: Extracts skills from text.
- **extract_education**: Extracts education information from text.
- **extract_work_experience**: Extracts work experience information from text.

### Aggregation and Formatting Functions

- **extract_details**: Aggregates all extraction functions to process a resume.
- **format_extracted_data**: Formats the extracted data for display.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [NLTK](https://www.nltk.org/) for natural language processing.
- [spaCy](https://spacy.io/) for advanced NLP tasks.
- [Apache Tika](https://tika.apache.org/) for text extraction from various document formats.
- [docx2txt](https://pypi.org/project/docx2txt/) for DOCX file processing.
- [Flask](https://flask.palletsprojects.com/) for web application framework.
- [ngrok](https://ngrok.com/) for creating secure tunnels to localhost.
