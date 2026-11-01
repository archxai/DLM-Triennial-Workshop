# 🚀 DLM Triennial ArchXAI Workshop: Getting Started

Welcome to the workshop! We have provided a pre-configured environment so you can focus on the AI and data rather than the infrastructure.

## 📦 Installation

You **do not** need to clone multiple repositories or configure complex environments manually. 

**The only thing you need to do is:**
1. **Download** the workshop `aj-dlm-workshop.zip` file.
2. **Extract** the contents into a folder on your computer (Note, no external drive).
3. **Run** the services using Docker (We'll go through these during the workshop but assumption is that you have Docker Desktop already installed). 

---

## 🛠️ What's Inside?

The workshop is divided into two main components:

### 🗄️ DB-Core (The "Memory")
**DB-Core** handles all the storage. Think of it as the warehouse for the project.
- **Image Storage**: Object storage, which saves your original and processed images.
- **Database**: Stores everything the AI finds: text transcriptions, bounding boxes (where the text is located), and document metadata.
- **Management**: Includes a web interface (Adminer) to let you browse the database tables visually.
- **Data retreiver**: A Web interface which can be used to download content from the DB

### 🧠 HTR-Core (The "AI recognizers")
**HTR-Core** is the AI engine that performs the actual work.
- **Text Detection**: It scans an image to find exactly where the lines of handwriting are.
- **Text Recognition**: It "reads" those handwritten lines and converts them into digital text.
- **Multi-Language**: It supports various languages (Finnish, Swedish, Estonian, Latvian, and Cyrillic).
- **User Interface**: Provides a simple web-based UI (Gradio) and APIdocs where you can upload an image and see the results.

---

## ⚡ Quick Start Summary

Once you have extracted the zip file:

1. **Start the Database first**: 
   `cd db-core` $\rightarrow$ `docker compose up --build -d`
2. **Start the AI Engine**: 
   `cd htr-core` $\rightarrow$ `docker compose up --build -d`
3. **Start Transcribing**: 
   Open `http://localhost:7860` in your browser!
