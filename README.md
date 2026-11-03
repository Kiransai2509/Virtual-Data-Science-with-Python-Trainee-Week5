# Week 5 — Deep Learning with TensorFlow/Keras

## Objective
Design, train and evaluate a feed-forward neural network for pre-call term-deposit subscription prediction.

## Files
- `YuvaIntern3_week5.ipynb` — executed TensorFlow notebook.
- `Week5_TensorFlow_Deep_Learning_Report.docx` — detailed report.
- `bank_marketing_neural_network.keras` — saved trained model.

## Architecture
- Dense layer: 128 units, ReLU.
- Batch normalization.
- Dropout: 0.35.
- Dense layer: 64 units, ReLU.
- Dropout: 0.25.
- Dense layer: 32 units, ReLU.
- Dropout: 0.15.
- Sigmoid output for binary classification.

Training used binary cross-entropy, Adam, class weights, early stopping and learning-rate reduction.

## Verified Test Results
- Accuracy: 0.8019.
- Precision: 0.3225.
- Recall: 0.6295.
- F1-score: 0.4265.
- ROC-AUC: 0.7873.
- PR-AUC: 0.4395.
- Early stopping at epoch 23; best weights restored from epoch 15.

## Evaluation
Training and validation loss/PR-AUC curves are used to assess overfitting. Test-set confusion matrix, ROC curve and precision-recall curve support error analysis.

## Leakage Prevention
`duration` is excluded because it is only available after the current call.

## Re-running
Open the notebook in Google Colab with TensorFlow available and select **Runtime → Run all**. The trained model is saved as `bank_marketing_neural_network.keras`.
