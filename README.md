# Protein-secondary-structure-prediction
PSSP using RF, LogReg, KNN and CNN models

This repository contains code, models, and analysis for predicting Q3 secondary structures (Helix, Sheet, Coil) from protein sequences using the CB513 dataset. The goal is to compare classical machine learning models and deep learning approaches to evaluate their effectiveness on this benchmark bioinformatics task.

CB513: A standard dataset used for secondary structure prediction.

Each sequence is labeled with one of three Q3 structure types:

H: Alpha-Helix
E: Beta-Sheet
C: Coil

Sliding window encoding was used to capture local sequence context for each residue.

Interpretation:

Random Forest outperforms all other models in terms of accuracy, showing it is the most reliable for this task.

CNN performs better than traditional ML models (LogReg, KNN), suggesting it captures local sequence features effectively.

KNN has the lowest accuracy, indicating it's not well-suited for high-dimensional, complex biosequence data like proteins.

ROC-AUC Scores

Random Forest generalizes best across all classes (C = Coil, E = β-strand, H = α-helix).

CNN shows better discrimination than traditional models, highlighting its deep learning advantage.

Class-wise Performance (Precision, Recall, F1-score)

1. Random Forest
   
High recall for class C (0.87) and precision for class E (0.85).
Balanced F1-scores around 0.77 overall.

3. CNN
   
Highest precision for class H (0.76) and good balance for others.
More balanced performance than KNN or Logistic Regression.

5. KNN
   
Poor precision and recall, especially for class E (recall: 0.35).
Often misclassifies class E as C or H.

7. Logistic Regression
   
Moderate performance across all classes.
Better recall for C and H than E.

Confusion Matrices

Random Forest: Mostly correct predictions along the diagonal. Some confusion between C & H and E & C.

CNN: More balanced than others. Slight confusion between E and C.

Logistic Regression: Misclassifies many H and E as C.

KNN: Most confusion, especially E misclassified as C and H.
