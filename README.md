## Problem Statement
The goal of this project/poc is to build a **blog recommendation system** that helps users find blogs similar to the ones they like. The system should:
- Analyze blog content to understand key topics and words.
- Identify and suggest blogs that have similar content.
- Give more importance to recent blogs so that newer content is recommended first.
- Ensure recommendations come from the same category as the selected blog.
- Allow users to interact and explore recommendations through a simple terminal interface.


## Blog Recommendation System Explanation

### 1. TF-IDF is used to convert blog content into numerical vectors.
- The **TF-IDF (Term Frequency-Inverse Document Frequency)** technique converts text data into numerical form by evaluating word importance.  
- This helps in comparing blogs based on their content rather than just keywords.  

### 2. Cosine similarity with NearestNeighbors finds similar blogs.
- The **NearestNeighbors model** uses **cosine similarity** to measure how similar two blogs are based on their TF-IDF vectors.  
- Blogs with closer cosine similarity scores are considered more relevant to each other.  

### 3. Time decay prioritizes recent blogs.
- A **time decay factor** is applied using an exponential function to reduce the importance of older blogs.  
- This ensures that newer blogs are given more weight in recommendations.  

### 4. Topic filtering ensures relevant recommendations.
- The system only recommends blogs that share the **same topic** as the selected blog.  
- This prevents suggesting irrelevant content, improving user satisfaction.  

### 5. Terminal-based interaction allows users to explore blog recommendations dynamically.
- Users can **input a blog ID** to get recommendations in an interactive terminal environment.  
- The system provides real-time recommendations, allowing users to explore similar content efficiently.  

## Evaluation Metrics

The two computed metrics evaluate different aspects of the blog recommendation system:

### **Precision at K (0.65)**

- Precision measures how many of the top **K** recommended blogs share the same topic as the selected blog.
- A precision of **0.65** means that, on average, **65.00% of the top 3 recommendations** belong to the same topic as the selected blog.
- This indicates a **moderate level of relevance** in recommendations.

### **Diversity Score (0.74)**

- Diversity measures how different the recommended blogs are from each other.
- A score of **0.74** means that the recommended blogs are **fairly diverse**, meaning they are not too similar to each other.
- This suggests the system provides **varied but still relevant recommendations** rather than overly redundant ones.

