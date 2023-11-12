# Group 13 CS4248 Machine Comprehension Model

Welcome to the Group 13 CS4248 repository! This project is a collaborative effort by a team of five dedicated individuals working on a machine comprehension model. Machine reading comprehension model takes in a Question and an associated Passage, and outputs a segment in the passage (A word, sentence or paragraph) containing the answer to the question.

Our goal is to explore the use of ensemble methods, to make an overall more effective model by selecting the highest performing models on a specific class of question based on some probability.

## Overview

In this repository, we employ a popular approach in Natural Language Processing (NLP) by leveraging frozen pre-trained models, such as BERT, ALBERT, and DistilBERT. 

In this repository, we employ 2 main techniques:
1. Transfer Learning and fine tuning on pre-trained models.
2. Freezing pre-trained models and training the a custom final layer.

The final layer helps our models better understand the context and generate more accurate answers to questions posed to them.


## Table of Contents

- [Repository Structure](#repository-structure)
- [Important Files](#important-files)
- [Usage](#usage)


## Repository Structure
- **/data:** Contains the squad v1.0 dataset.
- **/docs:** Documentation and team profiles .
- **/preds_for_ensemble:** Includes the predictions of individual models.
- **/scripts:** Contains utilitiy scripts for evaluation. 
- **/src:** Artifacts of code used to build our ensemble method.


## Important files
If you only want to run the final model, you only need the 2 files below.

Our model is split into 2 parts: 
1. predictions.py 
- Loads our models and collects the predictions of squad into a json file

2. ensemble.py 
- Takes in a json file and chooses the most appropriate model for each question based on our proprietary algorithm. 

## Usage

To get started with our machine comprehension model, follow these steps:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/YourUsername/Group_13_CS4248.git
   cd Group_13_CS4248
   ```

2. **Environment Setup:**

   Set up a Python environment and install the required packages. You can create a virtual environment to manage dependencies. Run the following command:

   ```bash
   pip install -r requirements.txt
   ```

3. **Download Pre-trained Models:**

   Download the pre-trained BERT, ALBERT, and DistilBERT models you intend to use. You can find these models on the Hugging Face Transformers library or other sources. Make sure to update the model paths in your code accordingly.

4. **Run the Model:**
   Run our model by executing both python models.
   
   ```
   python predictions.py output.json
   python ensemble.py output.json results.csv
   ```

Final predictions will be stored in results.csv.



