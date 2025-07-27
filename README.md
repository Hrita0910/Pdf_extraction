# PDF Outline Extractor

This tool extracts a clean, structured outline from PDF documents, including the **title** and **hierarchical headings (H1, H2, H3)**. It works **offline**, supports **multilingual documents**, and runs inside a lightweight **Docker container**.

## 🚀 Features

- 📑 Extracts Title + H1, H2, H3 headings
- 🌍 Multilingual support (e.g. Bengali, Japanese, English)
- 🧾 Output in clean JSON format
- 🐳 Runs completely offline in Docker (no internet access)

## 🛠 Folder Structure

Task_1A/
- ├── main.py          
- ├── Dockerfile       
- ├── requirements.txt 
- ├── input/          # Folder for input PDF files
- ├── output/         # Folder for output JSON files
- └── README.md       

## 📦 Prerequisites

- Docker Desktop installed and running
- Git (for pushing to GitHub)

## 📋 Setup Instructions (step-by-step)

- Step 1 : Clone or open the project

git clone https://github.com/Hrita0910/Pdf_extraction.git
cd Task_1A

- Step 2 : Build Docker Image

docker build -t pdf-outline-solution:latest .

- Step 3 : Run the container

docker run --rm `
  -v ${PWD}/input:/app/input `
  -v ${PWD}/output:/app/output `
  --network none `
  pdf-outline-solution:latest

## 🔧 Usage

- Step 1: Place your PDF files in the `input/` folder
- Step 2: Run the Docker container using Step 3 command
- Step 3: Check the `output/` folder for generated JSON files
- Step 4: Each PDF will have a corresponding JSON file with the same name

## 👨‍💻 Tech Stack

- Python 3.10
- pdfplumber
- Docker
- JSON output format


