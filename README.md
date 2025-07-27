# PDF Outline Extractor

This tool extracts a clean, structured outline from PDF documents, including the **title** and **hierarchical headings (H1, H2, H3)**. It works **offline**, supports **multilingual documents**, and runs inside a lightweight **Docker container**.

## 🚀 Features

- 📑 Extracts Title + H1, H2, H3 headings
- 🌍 Multilingual support (e.g. Bengali, Japanese, English)
- 🧾 Output in clean JSON format
- 🐳 Runs completely offline in Docker (no internet access)

## 🛠 Folder Structure

Task_1A/
├── main.py          
├── Dockerfile       
├── requirements.txt 
├── input/          # Folder for input PDF files
├── output/         # Folder for output JSON files
└── README.md       

## 📦 Prerequisites

- Docker Desktop installed and running
- Git (for pushing to GitHub)

## Setup Instructions (step-by-step)

- Step 1 : Clone or open the project

git clone https://github.com/your-username/Task_1A.git
cd Task_1A

- Step 2 : Build Docker Image

docker build -t pdf-outline-solution:latest .

- Step 3 : Run the container

docker run --rm `
  -v ${PWD}/input:/app/input `
  -v ${PWD}/output:/app/output `
  --network none `
  pdf-outline-solution:latest




