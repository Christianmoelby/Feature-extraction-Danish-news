# Feature-extraction-Danish-news

Contains essential code to scrape and collect Danish news and extract features from text, images, and faces. Formats features into a token-based dataset.

The code is developed in relation to the paper XXX. The paper contains appropriate citations of the components and on details of e.g. the dataset of faces to recognise. 

## 🚀 Project Overview

This repository includes a series of Jupyter notebooks that together:

1. **Collect Danish news content**  
2. **Extract various features**—textual, visual, facial, and scene-based—from the content  
3. **Format feature representations** into token-based datasets for downstream analysis or modeling

---

## 📂 Notebook Breakdown

Each notebook corresponds to one feature type or processing stage:

### 1. `Data generation.ipynb`  
- **Purpose**: Scrape and compile raw Danish news articles (text and images).  
- **Key steps**:  
  - Web scraping using Python (e.g., `requests`, `BeautifulSoup`)  
  - Storage of raw texts and images in structured folders/datasets  
- **Usage**: Run top-to-bottom to build raw data directory structure.

### 2. `Textual features.ipynb`  
- **Purpose**: Extract NLP-based features from article text.  
- **Techniques**:  
  - Tokenization  
  - mRAKE
- **Output**: Textual feature vectors per article ready for modeling.

### 3. `Facial_features.ipynb`  
- **Purpose**: Detect and vectorize faces present in images.  
- **Tools**: Deepface
- **Output**: Embedding vectors corresponding to detected faces in news images.

### 4. `Scene_tagging.ipynb`  
- **Purpose**: Analyze overall image scenes (e.g., indoor/outdoor, crowd, etc.).  
- **Tools**: OLLAMA
- **Output**: Scene classification tags as vectors for each image.

### 5. `Translate.ipynb`  
- **Purpose**: Fast translate of ENG image tags to DK.  
- **Output**: DK tokens.

### 6. `Compiling tokings.ipynb`  
- **Purpose**: Combine all previous feature outputs into a unified, tokenized dataset.  
- **Process**:  
  - Merge textual, visual, facial, and scene features  
  - Assign tokens/pointers to each feature group  
  - Output final structured dataset (CSV)

---

## 📚 Recommended Citation

If you use this repository or dataset, please cite:

**Mølby, C. A., & Bremholm, K. A. H. (2025).** *Feature extraction – GitHub repository*. GitHub.  
https://github.com/Christianmoelby/Feature-extraction-Danish-news  

We reserve the right to continuously update and maintain the repository.



