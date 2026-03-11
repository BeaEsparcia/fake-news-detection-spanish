# Detecting Fake News in Spanish with Classical NLP

This project explores whether simple natural language processing techniques can detect patterns associated with misinformation in Spanish news articles.

Using the *Spanish Fake News Corpus*, we train and evaluate classical machine learning models based on **TF-IDF features** to classify news as true or fake.

The goal is not to determine factual truth, but to analyze whether linguistic and stylistic patterns associated with misinformation can be captured by simple models.

---

## Dataset

The project uses the *Spanish Fake News Corpus Version 2.0 [[ FakeDeS Task @ Iberlef 2021 ]]*, developed for research on misinformation detection in Spanish.

The dataset contains news articles labeled as *true* or *fake*, collected from online media sources and fact-checking websites.

Topics covered include:

•⁠  ⁠Politics  
•⁠  ⁠Society  
•⁠  ⁠Science  
•⁠  ⁠Covid-19    
•⁠  ⁠Environment    
•⁠  ⁠International    
•⁠  ⁠Sport   

Dataset access:

https://huggingface.co/datasets/sayalaruano/FakeNewsCorpusSpanish

---

## Methodology

The pipeline follows a classical NLP approach: 

1.⁠ ⁠Combine headline and article text  
2.⁠ ⁠Convert text to numerical representations using *TF-IDF*  
3.⁠ ⁠Train machine learning classifiers  

Two models were evaluated:

•⁠  ⁠*Logistic Regression* (baseline)  
•⁠  ⁠*Linear Support Vector Machine (SVM)*   

---

## Results

The baseline model achieved approximately:  

•⁠  ⁠*Accuracy:* ~70%

Results were similar across both models, suggesting that performance is primarily constrained by the dataset size and vocabulary distribution rather than the specific algorithm.  

---

## Model Interpretation    

Because linear models are interpretable, we examined the most influential terms associated with each class.

The analysis suggests that the classifier relies primarily on *stylistic and contextual cues*, rather than factual verification.

For example:  

•⁠  ⁠institutional or journalistic language tends to appear more often in true news  
•⁠  ⁠conversational or emotional language appears more frequently in fake news predictions  

---

## Error Analysis

Examples of misclassified headlines show that: 

•⁠  ⁠well-written fake news can resemble legitimate journalism  
•⁠  ⁠sensational but factual news may be classified as fake  

This highlights the limitations of purely text-based approaches.

---

## Limitations

Several limitations should be considered:   

•⁠  ⁠the dataset is relatively small     
•⁠  ⁠the model relies on vocabulary patterns specific to the dataset    
•⁠  ⁠misinformation detection cannot rely solely on textual features    

Automated systems should therefore be considered *tools to assist human fact-checkers*, rather than systems capable of determining truth.

---

## Installation

Clone the repository and install the required dependencies:

 ⁠bash  
git clone https://github.com/BeaEsparcia/fake-news-detection-spanish.git  
cd fake-news-detection-spanish  
pip install -r requirements.txt  

---

## Citation

If you use the dataset, please cite:

1. Gómez-Adorno, H., Posadas-Durán, J. P., Enguix, G. B., & Capetillo, C. P. (2021).  
Overview of FakeDeS at IberLEF 2021: Fake News Detection in Spanish Shared Task.  
Procesamiento del Lenguaje Natural, 67, 223–231.

2. Aragón, M. E., Jarquín, H., Gómez, M. M. Y., Escalante, H. J., Villaseñor-Pineda, L., Gómez-Adorno, H., ... & Posadas-Durán, J. P. (2020, September). Overview of mex-a3t at iberlef 2020: Fake news and aggressiveness analysis in mexican spanish. In Notebook Papers of 2nd SEPLN Workshop on Iberian Languages Evaluation Forum (IberLEF), Malaga, Spain.

3. Posadas-Durán, J. P., Gómez-Adorno, H., Sidorov, G., & Escobar, J. J. M. (2019). Detection of fake news in a new corpus for the Spanish language. Journal of Intelligent & Fuzzy Systems, 36(5), 4869-4876.
Dataset license: CC-BY-4.0

Dataset license: *CC-BY-4.0*
