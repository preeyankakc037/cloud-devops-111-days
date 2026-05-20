# Day 37: Machine Learning (AWS)


## Core Strategy for ML Questions

* Identify **input type**: text, speech, image, video, documents
* Identify **output needed**: analysis, conversion, prediction, chatbot, recommendation

---

## 📸 Image & Video

### Amazon Rekognition

* Detects: objects, faces, celebrities, unsafe content
* Works with: images + videos
* ⚡ Exam tip: If you see **face detection / moderation / labeling → Rekognition**

---

## 🎤 Speech & Language

### Amazon Transcribe

* Speech → Text
* Use case: subtitles, call transcription
* ⚡ “audio to text” → Transcribe

### Amazon Polly

* Text → Speech
* Use case: voice assistants, narration
* ⚡ “text to voice” → Polly

### Amazon Translate

* Language translation
* ⚡ “translate text between languages” → Translate

---

## 💬 Chatbots & Contact Center

### Amazon Lex

* Chatbots (uses ASR + NLU)
* Same tech as Alexa
* ⚡ “chatbot / conversational interface” → Lex

### Amazon Connect

* Cloud contact center
* Integrates with Lex for IVR bots
* ⚡ “call center / customer support system” → Connect

---

## 📝 Text Analysis (NLP)

### Amazon Comprehend

* Extracts: sentiment, entities, key phrases
* ⚡ “analyze text meaning” → Comprehend

---

## 📄 Document Processing

### Amazon Textract

* Extracts text + structured data from scanned docs (forms, tables)
* ⚡ “scan PDF / OCR with structure” → Textract

---

## 🤖 Machine Learning Platform

### Amazon SageMaker

* Build, train, deploy ML models
* Fully managed
* ⚡ “custom ML model” → SageMaker

---

## 📊 Predictions & Intelligence

### Amazon Forecast

* Time-series forecasting
* ⚡ “predict future demand/sales” → Forecast

### Amazon Personalize

* Real-time recommendations
* ⚡ “Netflix/Amazon recommendations” → Personalize

### Amazon Kendra

* Intelligent document search
* ⚡ “search across documents using ML” → Kendra

---

## 🚀 High-Yield Exam Shortcuts

* Image/video → Rekognition
* Speech → Transcribe / Polly
* Language → Translate / Comprehend
* Chatbot → Lex
* Contact center → Connect
* Documents → Textract
* Custom ML → SageMaker
* Forecasting → Forecast
* Recommendations → Personalize
* Search → Kendra


## Final 1-Line Memory Trick

"Knowing the input type + expected output = pick the AWS ML service"



## 🧪 Common Exam Traps

* Textract vs Comprehend → Textract = extract, Comprehend = analyze
* Lex vs Connect → Lex = bot, Connect = call center
* Transcribe vs Translate → Transcribe = speech→text, Translate = language→language

