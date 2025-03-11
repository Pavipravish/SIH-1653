# Smart India Hackathon Workshop
# Date:11/03/2025
## Register Number:212224040249
## Name: PRAVISH.J
## Problem Title
SIH 1653: Web based Selector-Applicant Simulation Software
## Problem Description
Background: Recruitment and Assessment Centre (RAC) under DRDO, Ministry of Defence carries out interviews for applications received against advertised vacancies and for promotion to next higher grade for scientific manpower inducted within DRDO. Description: The process of interviewing is a challenging task. An unbiased objective interviewing process helps identify the right talent. The basic process of an interview involves posing a set of questions by an interviewer and thereafter evaluating responses from candidates. Thus, the questions asked should be relevant and match the area/ expertise of the applicant and the responses should also be of relevance w.r.t. the question asked. Expected Solution: The proposed solution should provide experts as well as candidates a real life Board Room experience, starting with initial ice-breaking questions leading to in-depth techno-managerial (depending on the level of candidate) questions. It shall also be able to provide a quantifiable score for experts as well as the candidate for the relevancy of questions w.r.t. the area/ expertise of the applicant. Similarly, candidate responses should also be graded for relevancy w.r.t. the question asked, finally assisting in arriving at an overall score for the subject knowledge of the candidate and thus his/ her suitability against the advertised post.

## Problem Creater's Organization
Ministry of Defence

## Idea
A virtual interview platform that ensures an objective, unbiased, and relevant interviewing process using AI-powered Natural Language Processing (NLP) and Machine Learning (ML). The system will assist experts and candidates by:

Providing an interactive and structured interview experience.
Evaluating relevancy of questions posed by the interviewer.
Assessing responses of candidates based on accuracy, depth, and relevance.
Assigning a quantifiable score to measure candidate's subject knowledge and suitability.
Key Features
Virtual Board Room Experience

Simulated panel interview environment.
Ice-breaking questions to ease candidates into the interview.
Techno-managerial questions based on candidate’s expertise & job level.
AI-Driven Question Generation & Relevancy Scoring

System ensures that interviewers ask domain-relevant questions.
AI suggests context-aware questions based on candidate's expertise.
Scoring of questions based on their relevance to the role & candidate profile.
Candidate Response Evaluation

AI analyzes answers for correctness, depth, and relevance.
Provides a quantitative score for each response.
Checks logical consistency, technical depth, and managerial understanding.
Overall Candidate Suitability Score

Final score based on cumulative relevancy of questions & responses.
Provides automated insights to assist expert panel in decision-making.
Ensures fair and unbiased selection for advertised posts.
Technology Stack
NLP & ML Models – To analyze language, evaluate responses, and score relevance.
Knowledge Graphs – To ensure domain-specific question generation.
Speech-to-Text AI – For transcribing and analyzing verbal responses.
Scoring Algorithms – To quantify question and response relevance.
Cloud-based System – Secure, scalable, and accessible from anywhere.


## Proposed Solution / Architecture Diagram

![image](https://github.com/user-attachments/assets/dad8f798-870d-4d01-ae2d-a00096489a5d)

## Use Cases

![FWAD USER DIAGRAM](https://github.com/user-attachments/assets/58f11c9a-ca45-417e-8ff9-693478a7f05a)

## Technology Stack
1️⃣ Frontend (User Interface)
The frontend should offer an intuitive and interactive experience for both interviewers and candidates.
Recommended Technologies:

React.js (or Next.js) – Fast, scalable, and supports real-time updates.
Tailwind CSS / Material UI – Clean and responsive UI design.
WebRTC / Socket.io – For live video interviews and real-time interactions.
Framer Motion – Smooth animations for a realistic boardroom experience.
Features:

Panel dashboard for experts.
Candidate interface with guided questions.
Real-time interview flow with AI-suggested questions.
Live scoring and feedback visualization.
2️⃣ Backend (APIs & Business Logic)
The backend will handle AI processing, scoring, and data storage securely.
Recommended Technologies:

Node.js (Express.js) or Python (FastAPI / Django) – Scalable backend framework.
GraphQL / REST API – Efficient data retrieval and flexible queries.
Redis – Caching system for faster responses.
Features:

AI-based question generation & evaluation logic.
Score calculation & ranking algorithms.
Role-based authentication (Experts, Candidates, Admins).
Secure API integration with DRDO’s HRMS system.
3️⃣ AI/ML Models (Interview Analysis & Scoring)
AI will assist in question relevance assessment, candidate response grading, and overall scoring.
Recommended Technologies:

NLP Models (Transformers - BERT/GPT-based fine-tuned models) – To analyze and score responses based on relevance.
OpenAI / Hugging Face Models – Pretrained models for natural language understanding.
SpaCy / NLTK – Text processing and sentiment analysis.
MLFlow – Model tracking and versioning.
PyTorch / TensorFlow – For deep learning-based evaluation models.
Features:

AI-powered question relevancy scoring (expert’s question vs. candidate’s expertise).
Response grading based on technical depth, correctness, and coherence.
Final interview score calculation using weighted scoring algorithms.
4️⃣ Database (Storage & Data Management)
To store interview records, scores, and user data securely.
Recommended Technologies:

PostgreSQL / MySQL – Relational DB for structured data storage.
MongoDB – For semi-structured interview logs.
Elasticsearch – Fast indexing & search for question banks.
S3 / Cloud Storage – Securely store video interview recordings (if required).
Features:

Candidate profiles & interview history.
AI-generated interview questions repository.
Scoring logs and analytics data.
5️⃣ DevOps & Deployment
Ensuring smooth deployment, scaling, and monitoring.
Recommended Technologies:

Docker & Kubernetes – Containerization and auto-scaling.
AWS / Azure / GCP – Cloud hosting & AI model serving.
CI/CD (GitHub Actions / Jenkins) – Automated deployment pipelines.
Prometheus & Grafana – Monitoring and real-time dashboarding.


## Dependencies
1️⃣ Infrastructure Dependencies
✔ Cloud / On-Premise Deployment – Depending on security policies, the system may be hosted on DRDO’s private cloud or government-approved data centers (e.g., NIC, AWS GovCloud, BharatNet).
✔ High-Performance Servers – Required for AI processing and real-time assessments.
✔ Database Management System (DBMS) – PostgreSQL / MongoDB for structured and unstructured data storage.

2️⃣ AI & ML Dependencies
✔ NLP Models for Question & Answer Evaluation

Pretrained Transformer Models (BERT, GPT, T5, or custom DRDO NLP models).
Hugging Face API or local fine-tuned models for response grading and question relevancy analysis.
✔ Machine Learning Pipeline

Model training and versioning (MLflow, TensorFlow Serving).
Data annotation tools for training models on scientific/defense-related interview datasets.
✔ Speech & Sentiment Analysis (Optional for Verbal Interviews)

Whisper / DeepSpeech for speech-to-text transcription.
VADER / SentimentIntensityAnalyzer for tone & confidence scoring.
3️⃣ Data Dependencies
✔ Structured Question Bank

Predefined and dynamically generated ice-breaking & technical questions.
Categorized by domain expertise & job levels (Junior, Mid, Senior).
✔ Candidate Profile Data

Secure integration with HRMS/Recruitment Database for fetching candidate details.
Ensuring domain-specific interview customization.
✔ Scoring Metrics & Benchmarks

Defining weightage for different evaluation criteria (question relevance, answer depth, technical correctness).
Benchmarking subject matter expertise scores for various DRDO positions.
4️⃣ Security & Compliance Dependencies
✔ End-to-End Encryption (E2EE)

All communication (text, voice, video) should be encrypted for confidentiality.
AES-256 encryption for stored data.
✔ Role-Based Access Control (RBAC)

Experts, Candidates, and Admins should have different access levels.
Audit logs for transparency in the interview process.
✔ Authentication & Authorization

SSO & OAuth 2.0 authentication for DRDO employees.
Multi-Factor Authentication (MFA) for added security.
✔ Government Compliance & Data Privacy

Adherence to India’s Data Protection Laws (DPDP Act 2023).
Compliance with Ministry of Defence cybersecurity policies.
5️⃣ Third-Party & External Integrations
✔ Speech-to-Text APIs – Google Speech, DeepSpeech, or OpenAI Whisper for transcribing responses.
✔ WebRTC / Zoom SDK / Jitsi – For secure real-time video interviews.
✔ AI Question Generator (GPT-based) – For dynamic interview structuring.
✔ HRMS & Applicant Tracking System (ATS) Integration – To fetch job descriptions & candidate profiles.

📌 Summary of Dependencies
Dependency Area	Key Dependencies

