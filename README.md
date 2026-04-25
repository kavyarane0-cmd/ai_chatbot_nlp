#AI Chatbot using NLP (Rule Based + Keyword Matching)

## 📌 Overview
This project implements a simple AI chatbot using basic Natural Language Processing (NLP) techniques.  
The chatbot interacts with users and responds to queries using:
- Rule-Based approach (FAQ system)
- Keyword Matching approach (dynamic responses)

## 🛠️ Technologies Used
- Python 3  
- NLTK (Natural Language Toolkit)  
- Google Colab / VS Code  

## ⚙️ Features
- Answers predefined FAQ questions  
- Handles flexible queries using keyword matching  
- Interactive chatbot in console  
- Easy to understand and implement  

## 🧠 Concepts Used
- Natural Language Processing (NLP)  
- Rule-Based Chatbot  
- Keyword Matching  
- Pattern Recognition

##Code
```
import nltk
nltk.download('punkt')

#rule based chatbot
faq_answers={
    "hi": "Hi, I am an AI chatbot. Ask me anything!!",
    "what is ai": "AI stands for Artificial Intelligence. It allows machines to perform tasks that normally require human intelligence.",
    "what is nlp": "NLP stands for Natural Language Processing. It helps computers understand and process human language.",
    "what is chatbot": "A chatbot is a software program that can communicate with users through text or voice.",
    "what is machine learning": "Machine Learning is a branch of AI where machines learn from data and improve performance automatically.",
    "what is deep learning": "Deep Learning is a subset of Machine Learning that uses neural networks to solve complex problems."
}

print("FAQ Chatbot started!")
print("Ask a question. Type 'bye' to exit.")

while True:
    user_input=input("You: ").lower().strip()

    if user_input=="bye":
        print("Bot: Goodbye!")
        break

    if user_input in faq_answers:
        print("Bot:",faq_answers[user_input])
    else:
        print("Bot: Sorry, this question is not available in my FAQ list.")

#chatbot using keyword matching

print("Keyword Chatbot started!")
print("Type 'bye' to exit.")

while True:
    user_input=input("You: ").lower()

    if "bye" in user_input or "exit" in user_input:
        print("Bot: Goodbye! Have a nice day.")
        break

    elif "hello" in user_input or "hi" in user_input or "hey" in user_input:
        print("Bot: Hello! How can I help you today?")

    elif "ai" in user_input:
        print("Bot: AI is used to make machines intelligent and capable of decision-making.")

    elif "nlp" in user_input:
        print("Bot: NLP helps computers understand, interpret, and respond to human language.")

    elif "chatbot" in user_input:
        print("Bot: A chatbot can answer user queries automatically using rules or AI techniques.")

    elif "name" in user_input:
        print("Bot: I am your AI lab chatbot.")

    elif "help" in user_input:
        print("Bot: You can ask me about AI, NLP, chatbot, machine learning, or deep learning.")

    elif "thank" in user_input:
        print("Bot: You're welcome!")

    else:
        print("Bot: I understood your message, but I do not have a proper answer for that yet.")
```
