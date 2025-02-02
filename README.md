# topsis-to-find-best-pretrained-model-for-Text-Conversational
topsis to find best pretrained model for Text Conversational 
# Evaluation of Pre-trained Text Conversational Models Using TOPSIS

## Overview
This assignment focuses on evaluating the performance of five pre-trained text conversation models in the field of natural language processing. The selected models include:
- GPT-3
- BERT
- T5
- DialoGPT
- BART

The assessment is conducted based on various key parameters, namely:
- **BLEU** (Bilingual Evaluation Understudy)
- **Rouge-L** (Longest Common Subsequence-based metric)
- **Coherence Score**
- **Rouge-1** (Overlap-based metric)
- **Response Length**

The Technique for Order of Preference by Similarity to Ideal Solution (TOPSIS) is used to rank these models. TOPSIS is a multi-criteria decision-making method that determines the best alternative based on its closeness to an ideal solution and its distance from a negative ideal solution.

## Methodology
The steps followed in the analysis are as follows:

1. **Data Collection:**  
   The data is stored in a CSV file (`input.csv`) with columns for each evaluation metric.

2. **Normalization:**  
   The decision matrix is normalized using the Euclidean norm. This step ensures that the criteria (which may have different units) are comparable.

3. **Weighted Normalization:**  
   Each criterion is assigned an equal weight (since no specific weighting is provided) and the normalized values are multiplied by these weights.

4. **Determine Ideal Solutions:**  
   For benefit criteria (all metrics in this assignment), the ideal best is the maximum value for each criterion and the ideal worst is the minimum value.

5. **Distance Calculation:**  
   The Euclidean distances from the ideal best and worst are calculated for each model.

6. **TOPSIS Score Calculation:**  
   The relative closeness of each alternative to the ideal solution is computed, resulting in the TOPSIS score:
   TOPSIS Score = D_negative / (D_positive + D_negative)


8. **Ranking:**  
   Models are ranked based on the TOPSIS score (the higher the score, the better the performance).

9. **Visualization:**  
   A bar plot is generated to visually compare the TOPSIS scores of the different models.

## Files Included
- `topsis_analysis.py`: Python script implementing the TOPSIS method.
- `input.csv`: Input CSV file containing the evaluation metrics for the pre-trained models.
- `topsis_output.csv`: Output CSV file containing the original data along with the computed TOPSIS scores and corresponding ranks.
- `topsis_scores.png`: Bar plot visualizing the TOPSIS scores.
- `README.md`: This README file detailing the assignment, methodology, and file descriptions.

## Instructions
1. Place the `input.csv` file in the same directory as the `topsis_analysis.py` script.
2. Run the script using Python 3:
