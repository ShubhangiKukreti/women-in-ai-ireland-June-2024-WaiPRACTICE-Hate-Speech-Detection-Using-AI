---
layout: default
---

# Hate Speech Detection Using AI: A Comprehensive Approach with BERT, LLMs, and Logistic Regression

## Introduction

In recent years, the proliferation of hate speech on social media platforms has become a significant concern. Detecting and mitigating such harmful content is crucial for maintaining a healthy online environment. With advancements in AI, particularly in Natural Language Processing (NLP), it's possible to automate the detection of hate speech with high accuracy. In this project, we explore a hybrid approach that leverages traditional machine learning techniques like Logistic Regression, as well as advanced models like BERT and GPT-4, to build a robust meta-model for hate speech detection.

## Project Overview

### Objective

The primary goal of this project is to develop an AI-driven system capable of accurately detecting hate speech in text data. By integrating traditional machine learning methods with state-of-the-art models, we aim to enhance detection accuracy and create a model that can be applied in real-world scenarios, where understanding the context and nuances of language is crucial.

### Dataset

For this project, we used the "Hate Speech and Offensive Language Dataset" available on Kaggle. This dataset contains tweets labeled as "hate speech," "offensive language," or "neither." The dataset's diversity makes it an ideal candidate for training models that need to differentiate between various levels of offensive content.

### Methodology

#### 1. Data Exploration and Preprocessing

Before diving into model training, it was essential to understand the data. We conducted an extensive Exploratory Data Analysis (EDA) to examine the distribution of classes and the common words associated with each class. This step helped us gain insights into the characteristics of hate speech and offensive language.

**Key Preprocessing Steps:**
*  **Text Cleaning:** Removed special characters, URLs, Twitter handles, and stop words to ensure the models focused on the core content.
  
*  **Tokenization and Lemmatization:** Converted text into tokens and applied lemmatization to reduce words to their base forms, enhancing the model's ability to generalize.

#### 2. Traditional Machine Learning Approach

**Logistic Regression**

As a baseline, we implemented a traditional machine learning approach using Logistic Regression. This method is simple yet effective for binary classification tasks. After vectorizing the text data using techniques like TF-IDF and Bag of Words, we trained a Logistic Regression model to classify tweets.

The Logistic Regression model provided a solid foundation and baseline accuracy, helping us understand the complexity of the task and the need for more advanced models.

#### 3. Advanced Model Deployment

**BERT Fine-Tuning**

We fine-tuned a pre-trained BERT model on our dataset. BERT's ability to understand the context within text made it an excellent choice for this task. After training, the BERT model provided predictions that were directly compared to the Logistic Regression outputs to assess the performance improvement.

**Intergrating LLM via API**

In parallel, we utilized GPT-4 for zero-shot classification using the OpenAI API. GPT-4's extensive training on a diverse range of internet text made it adept at understanding the nuances of language, even without specific training on our dataset.

The predictions from GPT-4 were used to analyze how well a large language model, without specific fine-tuning, could perform on the task compared to the fine-tuned BERT model and traditional Logistic Regression.

#### 4. Model Evaluation

Each model was evaluated on a validation set, with performance metrics such as accuracy, precision, recall, and F1-score being computed. This step was crucial in understanding the effectiveness of our approaches and identifying areas for further improvement.

### Results and Discussion

The results from our experiments showed that while the Logistic Regression model provided a strong baseline, the BERT model significantly improved classification accuracy due to its deep understanding of context. GPT-4, even without fine-tuning, offered valuable insights and competitive performance, demonstrating the power of large language models in NLP tasks.

### Challenges


### Conclusion


### Future Work

Looking ahead, we plan to explore a meta-model approach that combines the predictions from multiple models, including Logistic Regression, BERT, and GPT-4. This ensemble technique could potentially enhance the overall performance by leveraging the strengths of each model.

Additionally, applying this model to other datasets or even live social media data could provide more insights and opportunities for refinement. We also aim to explore other LLMs and advanced ensemble techniques to further improve the model's performance.

### Acknowledgements

Special thanks to our mentor, [Nabanita Roy](https://www.linkedin.com/in/nabanita-roy/), for guiding us through this project and to the women in Ireland community for providing the resources and support necessary to bring this project to life.



