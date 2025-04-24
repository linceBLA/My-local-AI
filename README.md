# My local AI
# 🧠 How I Built My Own Local AI (And You Can Too!)

Artificial Intelligence is becoming part of our daily lives! From writing emails to planning meals, it's everywhere.  
And what's cooler than having your own local AI running privately, securely, and for free on your computer?

📄✨ One of the coolest things about having your own local AI is that you can **upload your personal notes**!  
From there, you can:

- 🧠 **Extract everything you’ve written about a specific topic**
- 📝 **Generate an article based on your content**
- 🔍 **Search through your notes instantly**

It’s like having a superpowered assistant that knows all your stuff!


Thanks to this awesome video by NetworkChuck, I was able to install my own AI assistant using **Ollama** and **Open WebUI**. It’s not complicated — all you need is a Linux machine (or WSL on Windows) with a GPU, and you’re good to go.

---

## 🛠️ Step-by-Step Installation (Kali Linux / Linux)

> 💡 **For Windows users:** Use WSL (Windows Subsystem for Linux) and follow the same steps!

### 1. Install Ollama
- Go to [ollama.ai](https://ollama.ai) and download the Linux version.  
- Then open your terminal in the folder where the file is located and run:

```bash
curl -fsSL https://ollama.com/install.sh | sh
```



---

### 2. Test Ollama
- Open your browser and go to:

```arduino
http://localhost:11434
```

If you see a message saying “Ollama is running” — congrats! 🎉 You’re ready to move on.

---

### 3. Pull Your First AI Model
- Go to [ollama.com/models](https://ollama.com/models) to explore different AI models.  
- Choose the one that suits your needs.

For example, to use **OpenHermes**, run:

```bash
ollama pull openhermes
```



---

### 4. Start Chatting with Your AI
```bash
ollama run openhermes
```



You can now chat directly with your AI in the terminal!  
To end the chat:

```bash
/bye
```



To list all downloaded models:

```bash
ollama list
```



---

## 🌐 Add a Web Interface with Open WebUI
To use your AI in a browser instead of the terminal, install **Open WebUI**.

⚠️ **You need Docker**

### Install commands:
```bash
sudo docker run -d --network=host -v open-webui:/app/backend/data -e  OLLAMA_BASE_URL=http://127.0.0.1:11434 -e ENABLE_DOCUMENTS=true --name open-webui --restart always ghcr.io/open-webui/open-webui:main 
```

Then go to your browser and open:

```arduino
http://localhost:8080
```

If it’s your first time, sign up for an account.

🎉 _Boom! You now have a browser-based local AI!_

![image](https://github.com/user-attachments/assets/e9d1be49-1bb5-430c-8a93-d63254268c13)


Tips:
To upload your notes files, you need to create a knowledge (it's kind of the Documents tab of the previous version), and upload your documents there. You can refer to these documents in your prompt with #name-of-your-knowledge


---

## 🔄 Switch and Customize Models
Once inside **Open WebUI**, you can:

- **Ask questions for free** 🆓  
- **Change models anytime** 🧠  
- **Set your default model** to suit your style  

Click the dropdown on the right side of the search bar to switch models!

---

## ✅ Why You Should Have Your Own Local AI
- 🔒 **Privacy:** Your data stays on your machine.  
- 💸 **Free:** No subscription fees or token limits.  
- 🎯 **Customizable:** Choose models for creative writing, coding, research, and more.  
- 🧠 **Offline:** Works even without an internet connection (after setup)!
- 📝 **AI in your notes!:** upload your personal notes
