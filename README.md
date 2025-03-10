# Children's Tale Summarizer Flask App

This project provides summarized versions of children's tales using NLP techniques.

🔗 Related Projects
This project is part of a modular research framework for evaluating and improving fairy tale summarization models. Below are the related repositories:

| Children's Tale Summarizer - Flask App | The main Flask-based API that generates fairy tale summaries. (https://github.com/SinemCiftciDemirci/childrens-tale-summarizer-flask-app) |

| GPT Summarizer | Creates GPT-based fairy tale summaries. (https://github.com/SinemCiftciDemirci/gpt-summarizer) |

| Cosine Similarity Summarizer | Performs extractive summarization using cosine similarity. (https://github.com/SinemCiftciDemirci/cosine-similarity-summarizer) |

| Single Summary Evaluation | Measures the performance of a single summary using BERTScore and ROUGE score. (https://github.com/SinemCiftciDemirci/single-summary-evaluation) |

| Batch Summary Performance Evaluation | Compares model-generated summaries with GPT and Cosine-based reference summaries, calculating ROUGE and BERTScore collectively. (https://github.com/SinemCiftciDemirci/batch-summary-performance-evaluation) |

| Summary Performance Comparison | Creates visual performance comparisons from the Model_Performance.xlsx file produced in the Batch Summary Evaluation repo. (https://github.com/SinemCiftciDemirci/summary-performance-comparison) |

| Vision Model Test | Translates the generated summaries into English and creates three visuals: introduction, development, and conclusion. (https://github.com/SinemCiftciDemirci/vision-model-test) |

Each repository serves a **unique role** in evaluating or improving summarization models. You can use them **individually** or **together** for deeper analysis.


# Overview
This project is a Flask-based web application designed to summarize Turkish children's tales using AI-powered NLP models and generate corresponding illustrations using text-to-image models. The application processes each story by dividing it into three sections—Introduction, Development, and Conclusion—providing a summarized version and generating an illustration for each section.

# Features
- **Tale Summarization:** Automatically summarizes Turkish children's tales.
- **Image Generation:** Generates illustrations for each section of the story using an AI-powered text-to-image model.
- **File Upload:** Supports TXT and PDF file uploads.
- **English Translation:** Translates summaries into English to enhance visual generation.
- **User-Friendly Interface:** Clean and intuitive HTML/CSS interface for easy interaction.


# 📂 Project Structure

├── instance/ # Contains the SQLite database (summaries.db)
├── static/ # Static files (CSS, images) 
│ └── styles.css 
├── templates/ # HTML templates for the Flask
│ └──index.html
│ └──search.html
│ └──summary.html 
│ └──upload.html 

├── app.py # Flask web application entry point 
├── config.txt # API keys and model configurations 
├── config_loader.py # Loads configuration settings 
├── image_generator.py # Handles AI-based image generation 
├── requirements.txt # Required dependencies for the web app 
├── summarizer.py # Summarization logic for processing tales 



# 🛠 Installation & Setup
1️⃣ Install Dependencies
pip install -r requirements.txt

2️⃣ Run the Web Application
python app.py

The app will be accessible at local.

# 📑 Usage Guide
1. Upload a Story
Upload a TXT or PDF file containing a children's tale.

2. Summarization & Translation
The story is automatically summarized, divided into three sections (Introduction, Development, Conclusion), and translated into English.

3. Image Generation
Illustrations are generated for each section using a text-to-image model.

4. View Results:
Summaries and generated images are displayed on the interface and stored locally for further reference.

# 🔑 Configuration
Add your API keys and model configurations in the config.txt file:

SECRET_KEY= "your_secret_key"
HUGGINGFACE_API_KEY= "your_huggingface_api_key"
OPENAI_API_KEY= "your_openai_api_key"
SUMMARY_MODEL_NAME= "Turkish-NLP/t5-efficient-small-MLSUM-TR-fine-tuned"
TRANSLATION_MODEL_NAME= "Helsinki-NLP/opus-mt-tr-en"
IMAGE_MODEL_ID= "stable-diffusion-v1-5/stable-diffusion-v1-5"


# 📬 Contribution
Contributions are welcome! Feel free to:

Fork the repository
Submit a pull request
Report issues and suggest improvements

This README now focuses solely on the user interface and core functionality of the Flask web application. It excludes any performance evaluation or analysis details that will be handled in separate projects.
