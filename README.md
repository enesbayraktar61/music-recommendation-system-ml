# Music Recommendation System (Feature-Based)

This project builds a music recommendation system using feature-based similarity techniques.

The system suggests similar songs by analyzing numerical audio features such as danceability, energy, loudness, tempo, and valence. Cosine similarity is used to identify songs with similar characteristics.

---

## Project Overview

- **Problem Type:** Recommendation System  
- **Approach:** Content-Based Recommendation  
- **Technique Used:** Cosine Similarity  
- **Framework:** scikit-learn  
- **Deployment:** Streamlit  

---

## Dataset

The project uses a Spotify tracks dataset containing:

- Track name  
- Artist  
- Genre  
- Audio features such as:
  - Danceability  
  - Energy  
  - Loudness  
  - Tempo  
  - Valence  

Dataset size:

- Total songs: **114,000**

After preprocessing:

- Final dataset size: **81,343 songs**

---

## Data Preprocessing

### Feature Selection

We selected the most relevant numerical audio features:

- Danceability  
- Energy  
- Loudness  
- Tempo  
- Valence  

### Data Cleaning

- Removed missing values  
- Removed duplicate songs  

### Feature Scaling

Numerical features were standardized using:

- **StandardScaler**

This ensures fair similarity comparison across features.

---

## Modeling

This project uses a feature-based similarity approach.

### Feature Matrix

A numerical feature matrix was created using selected audio attributes.

### Similarity Computation

Similarity between songs was calculated using:

- **Cosine Similarity**

To avoid memory issues with large datasets, similarity is computed **on demand** rather than building a full similarity matrix.

---

## Results

The recommendation engine generates meaningful song suggestions.

Example:

Input: **Blinding Lights**

Recommendations:

- Overwhelm – Alphaxone  
- Remembering You – Tony O'Connor  
- Imipramine (Pt.1) – PERMEATE  
- Autumn (Solo Piano) – Ryan Stewart  
- Asmr: Big Air Conditioner – ASMR HD  

This demonstrates effective feature-based recommendation performance.

---

## Deployment

The cleaned dataset and scaled features were saved using pickle.

The Streamlit application allows users to:

- Select a song  
- Receive 5 similar recommendations  

---

## Conclusion

This project demonstrates how feature-based similarity methods can be applied to large-scale music datasets.

It highlights how numerical audio features can effectively drive recommendation systems without requiring user interaction data.

---

## How to Run Locally

git clone https://github.com/enesbayraktar61/music-recommendation-system-ml.git

cd music-recommendation-system-ml
pip install -r requirements.txt
streamlit run app.py

---
