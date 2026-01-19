# Text-mining-in-arxiv-abstracts
A Deep Learning-based "Divide and Conquer" framework designed to classify scientific papers from the arXiv repository into over 150 subcategories.

## The Challenge
Manual classification of scientific literature is becoming unsustainable due to the exponential growth of submissions. Traditional flat classification models often struggle with:
* High dimensionality of technical language.
* Extreme class imbalance.
* Semantic ambiguity between overlapping disciplines (e.g., Machine Learning in Computer Science vs. Statistics).

## The Solution: "Divide and Conquer"
Instead of a traditional flat classifier, this project implements a two-phase hierarchical architecture:

1. **Macro-Area Classifier**: A general model that directs documents to broad categories (Physics, Mathematics, Computer Science, Finance, etc.).
2. **Specialist Models**: A set of specialized classifiers that determine the final sub-category within each macro-area.

This approach effectively reduces the search space and improves accuracy by allowing models to learn the specific nuances of each scientific domain.

## Methodology & Tools
* **Data Source**: A dataset of arXiv metadata (titles and abstracts) processed to handle more than 150 labels.
* **Text Representation**: Exploration of techniques from Bag of Words (BoW) to deep contextual embeddings.
* **Architecture**: Hierarchical classification implemented in Python.
* **Optimization**: Use of specialist models to handle inter-disciplinary ambiguity.

## Project Structure
The repository is organized to follow the data science lifecycle:
* `exploration.ipynb`: Initial analysis of the arXiv metadata and label distribution.
* `preprocess.ipynb`: Text cleaning and preparation for the hierarchical pipeline.
* `baseline.ipynb`: Benchmarking traditional classification approaches.
* `model_a.ipynb` & `model_b.ipynb`: Implementation of the Macro and Specialist deep learning models.

---
Developed as part of a research project at the Universidad Autónoma de Baja California (UABC).
