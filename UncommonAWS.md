These are exactly the kinds of **uncommon AI/ML service questions** that show up on CLF-C02. The trick is usually recognizing **one keyword** and immediately mapping it to the service.

---

# Q537 — Identify Employees from Video

> A company wants to use automated video analysis to identify employees that are accessing its offices.

A. Amazon Rekognition ✅
B. Amazon Polly
C. Amazon Cognito
D. AWS Lambda

### Keyword

**video analysis** + **identify people**

### Why Rekognition?

* Facial recognition
* Object detection
* Video/image analysis

### Eliminate

| Service | Purpose             |
| ------- | ------------------- |
| Polly   | Text → Speech       |
| Cognito | User authentication |
| Lambda  | Run code            |

### Memory Tip

**"Recognition" → Rekognition**

---

# Q598 — Chatbot

> A company wants to add a conversational chatbot to its website.

A. Amazon Textract
B. Amazon Lex ✅
C. AWS Glue
D. Amazon Rekognition

### Keyword

**chatbot**, **conversation**

### Why Lex?

Lex powers conversational interfaces (same technology as Alexa).

### Eliminate

| Service     | Purpose                     |
| ----------- | --------------------------- |
| Textract    | Extract text from documents |
| Glue        | ETL                         |
| Rekognition | Images/video                |

### Memory Tip

**Lex = Alexa's chatbot engine**

---

# Q632 — Meeting Notes

> Which AWS service uses speech-to-text conversion to help users create meeting notes?

A. Amazon Polly
B. Amazon Textract
C. Amazon Rekognition
D. Amazon Transcribe ✅

### Keyword

**speech-to-text**

### Why Transcribe?

Converts spoken audio into text.

### Eliminate

| Service     | Purpose                  |
| ----------- | ------------------------ |
| Polly       | Text → Speech            |
| Textract    | Document text extraction |
| Rekognition | Image/video analysis     |

### Memory Tip

**Transcribe = Audio → Text**

---

# Q649 — Organize and Search Images

> Which AWS service should a company use to organize, characterize, and search large numbers of images?

A. Amazon Transcribe
B. Amazon Rekognition ✅
C. Amazon Aurora
D. Amazon QuickSight

### Keyword

**images**

### Why Rekognition?

Can detect:

* Objects
* Faces
* Labels
* Activities

### Exam Shortcut

If the question contains **photos, faces, video, objects**, pick **Rekognition**.

---

# Q320 — Search Text in Documents

> A company needs to search for text in documents stored in Amazon S3.

A. Amazon Kendra ✅
B. Amazon Rekognition
C. Amazon Polly
D. Amazon Lex

### Keyword

**search documents**

### Why Kendra?

Enterprise intelligent search service.

### Eliminate

| Service     | Purpose |
| ----------- | ------- |
| Rekognition | Images  |
| Polly       | Speech  |
| Lex         | Chatbot |

### Memory Tip

**Kendra = Google for your company documents**

---

# Q328 — Convert Text to Voice

> Which AWS service converts text to lifelike voices?

A. Amazon Transcribe
B. Amazon Rekognition
C. Amazon Polly ✅
D. Amazon Textract

### Keyword

**text to voice**

### Why Polly?

Creates natural-sounding speech.

### Common Trap

| Service    | Direction     |
| ---------- | ------------- |
| Polly      | Text → Speech |
| Transcribe | Speech → Text |

### Memory Tip

Think of a **parrot ("Polly") talking**.

---

# Other Services You Should Know

## Textract

**Keyword:** scanned forms, PDFs, invoices, OCR

Example:

> Extract text from scanned invoices

✅ Textract

---

## Comprehend

**Keyword:** sentiment, entities, language analysis

Example:

> Analyze customer reviews to determine positive or negative sentiment

✅ Comprehend

### Memory Tip

**Comprehend = Understand text**

---

## Personalize

**Keyword:** recommendations

Example:

> Recommend products based on customer behavior

✅ Personalize

---

## Kendra

**Keyword:** enterprise search

Example:

> Search across company documents

✅ Kendra

---

# The 30-Second AI/ML Cheat Sheet

| If You See...           | Answer      |
| ----------------------- | ----------- |
| Text → Speech           | Polly       |
| Speech → Text           | Transcribe  |
| Chatbot                 | Lex         |
| Photos, Faces, Video    | Rekognition |
| Scanned PDFs, OCR       | Textract    |
| Sentiment Analysis      | Comprehend  |
| Product Recommendations | Personalize |
| Enterprise Search       | Kendra      |
| Build ML Models         | SageMaker   |
| Forecast Future Demand  | Forecast    |

### Super-High Yield Pairings

The exam loves these opposites:

* **Polly** = Text → Speech
* **Transcribe** = Speech → Text

and

* **Textract** = Extract text from documents
* **Comprehend** = Understand the meaning of that text

If you memorize just those four distinctions, you'll answer most of the uncommon AI-service questions correctly.
