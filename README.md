# Local AI Deployment

This project demonstrates how to install and run your own local AI agent directly on your computer, ensuring full data privacy, speed, and control over your environment.

---

## Why Deploy a Local AI?

- **Full ownership of data**
- **Zero dependency on cloud services**
- **Enhanced privacy and security**
- **Search through your notes instantly**

---

## Table of Contents

- [Project Overview](#project-overview)
- [Installation Guide](#installation-guide)
- [Key Features](#key-features)
- [Use Cases](#use-cases)

---

## Project Overview

This project uses:

- **Ollama** – Lightweight LLM (Large Language Model) runtime, operating locally.
- **Open WebUI** – A browser-based interface to interact easily with your local AI.

By following this guide, you can install and interact with powerful language models entirely offline and securely.

---

## Installation Guide

### Requirements

- Linux OS (tested on Kali Linux)
- Docker installed
- Basic terminal knowledge

### Step 1: Install Ollama

Visit the official Ollama website and download the Linux version.

Follow the installation instructions provided on the site.

Alternatively, install directly via terminal:

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### Step 2: Verify Ollama Installation

Open your browser and navigate to:

```arduino
http://localhost:11434
```

If you see the Ollama service running, the installation is successful.

### Step 3: Pull a Language Model

You must download at least one model to start using Ollama.  
Visit the Ollama Models Library and choose the model you need.

Example to pull `llama3`:

```bash
ollama pull llama3
```

### Step 4: Start Chatting with Your AI in the Terminal

Once a model is installed, you can interact with it directly from the command line.

Example:

```bash
ollama run llama3
```

You can now start asking questions and receiving answers directly within your terminal.  
To end the chat:

```bash
/bye
```


To list all downloaded models:

```bash
ollama list
```


### Step 5: Deploy Open WebUI (Optional - Browser Interface)

If you prefer interacting via a web interface, you can deploy Open WebUI.

Run the following Docker command:
```bash
sudo docker run -d --network=host -v open-webui:/app/backend/data -e  OLLAMA_BASE_URL=http://127.0.0.1:11434 -e ENABLE_DOCUMENTS=true --name open-webui --restart always ghcr.io/open-webui/open-webui:main 
```

This will:

- Launch the interface on port 8080
- Save user data inside a Docker volume

### Step 6: Access Open WebUI

Open your browser and visit:

```arduino
http://localhost:8080
```

If it’s your first time, sign up for an account.

Select your model, start chatting, and enjoy a full browser experience, still fully local and private.

Tips:
To upload your notes files, you need to create a knowledge (it's kind of the Documents tab of the previous version), and upload your documents there. You can refer to these documents in your prompt with #name-of-your-knowledge

---

## Key Features

- 🖥️ **Fully Local Operation**: No external API calls.
- 🔒 **Enhanced Privacy**: Data remains on your machine.
- 🛠️ **Customizable Models**: Switch models according to needs.
- 🌐 **Browser-Based UI**: User-friendly experience with Open WebUI.

---

## Use Cases

- 📚 **Research Assistant**: Summarize notes, articles, and papers offline.
- 🛡️ **Secure Work Environments**: Operate AI in air-gapped or privacy-critical areas.
- 📝 **Content Generation**: Draft emails, reports, or articles without external exposure.
- 🔍 **Knowledge Management**: Upload and query your own private documents locally.

---


📎 **Ref**: [open-webui GitHub Repository](https://github.com/open-webui/open-webui)




