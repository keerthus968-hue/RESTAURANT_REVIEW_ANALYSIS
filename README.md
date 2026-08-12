# Restaurant Review Analysis using Generative AI

## Project Overview

**Restaurant Review Analysis using Generative AI** is a Natural Language Processing case study that uses a Large Language Model (LLM) to analyze customer reviews and generate meaningful, actionable insights from unstructured restaurant feedback. The project demonstrates how Generative AI can be used not only for sentiment classification but also for **aspect-level analysis, feature extraction, and automated customer response generation**.

The project uses a dataset containing **20 restaurant reviews and 3 columns**, with no missing values. The **Mistral-7B-Instruct-v0.1** model from Hugging Face is integrated using the Transformers library and loaded with **8-bit quantization** to reduce memory usage and support efficient inference.

## Objective

The primary objective is to build a multi-stage AI-powered review analysis pipeline that can understand customer feedback at different levels. The project analyzes overall sentiment, identifies sentiment toward specific restaurant experience aspects, extracts the features customers liked or disliked, and generates personalized responses based on the review.

## Methodology

The project begins with data loading and exploration using **Pandas**, followed by checking the dataset structure, dimensions, and missing values.

The **Mistral-7B-Instruct-v0.1** Large Language Model is loaded from Hugging Face using **AutoTokenizer** and **AutoModelForCausalLM**. The model uses **8-bit quantization**, FP16 computation, and automatic device mapping to optimize resource utilization.

A reusable query function is developed to interact with the LLM using system instructions and customer review text. The model is configured to generate structured outputs using controlled parameters such as **temperature, top-p, attention masks, and maximum output tokens**.

## Multi-Stage Review Analysis

### 1. Overall Sentiment Analysis

Each restaurant review is classified into **Positive, Negative, or Neutral** sentiment.

The analysis shows that **negative sentiment slightly outweighs positive and neutral feedback**, with:

* **8 Negative reviews**
* **6 Positive reviews**
* **6 Neutral reviews**

### 2. Aspect-Level Sentiment Analysis

The project further analyzes sentiment across three key aspects of the restaurant experience:

* **Food Quality**
* **Service**
* **Ambience**

The results indicate that:

* **Food Quality:** 8 Negative, 6 Positive, 5 Neutral, 1 Not Applicable
* **Service:** 10 Negative, 8 Positive, 2 Neutral
* **Ambience:** 8 Positive, 6 Neutral, 1 Negative, 5 Not Applicable

The analysis identifies **Service as the most criticized aspect**, while **Ambience emerges as the strongest positive driver**.

### 3. Feature Extraction

The LLM is then used to extract specific features that customers liked or disliked under **Food Quality, Service, and Ambience**.

Examples include concrete factors such as **taste, temperature, presentation, waiting time, staff behavior, lighting, and music volume**. This transforms general review text into detailed and actionable restaurant feedback.

### 4. Automated Customer Response Generation

The final stage uses Generative AI to create **polite and empathetic responses** for customers based on their review.

Positive reviews receive appreciation and encouragement to return, neutral reviews receive acknowledgement and an invitation to provide further feedback, while negative reviews receive an apology and assurance that the concerns will be reviewed.

## Key Insights

The project demonstrates that restaurant reviews can be analyzed at multiple levels using a Large Language Model. Instead of relying only on an overall sentiment score, the approach provides deeper insights into **what customers liked, what they disliked, which restaurant aspects require improvement, and how businesses can respond effectively**.

## Project Outcome

This case study demonstrates a practical **Generative AI-powered customer feedback analytics system** capable of converting unstructured restaurant reviews into structured business insights and personalized customer responses.

The multi-stage pipeline can help restaurants identify recurring service issues, understand customer preferences, prioritize operational improvements, and improve customer engagement through automated yet context-aware responses.

## Technologies Used

**Python | Pandas | JSON | Hugging Face Transformers | Mistral-7B-Instruct-v0.1 | PyTorch | Google Colab | Generative AI | Large Language Models (LLMs)**

**Project Focus:** Generative AI | NLP | LLM | Sentiment Analysis | Aspect-Based Sentiment Analysis | Feature Extraction | Customer Feedback Analytics | Automated Response Generation
