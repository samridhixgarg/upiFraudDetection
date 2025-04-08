# UPI Financial Fraud Detection

This project focuses on detecting fraudulent transactions in UPI (Unified Payments Interface) financial data using machine learning. A Random Forest Classifier is trained on a synthetic dataset to classify transactions as either legitimate or fraudulent.

## Project Structure

- **Dataset**: A fake dataset (`transactions.csv`) with fields like transaction ID, timestamp, sender/receiver info, amount, and transaction status.
- **Objective**: Identify patterns in transactions to classify whether a given transaction is fraudulent (`FAILED`) or legitimate (`SUCCESS`).
- **Approach**: Data preprocessing, visualization, model training, evaluation, and feature importance analysis.

## Dataset Columns

- `Transaction ID`: Unique ID for each transaction
- `Timestamp`: Date and time of transaction
- `Sender Name`: Name of sender
- `Sender UPI ID`: UPI ID of sender
- `Receiver Name`: Name of receiver
- `Receiver UPI ID`: UPI ID of receiver
- `Amount (INR)`: Transaction amount
- `Status`: Transaction result - `SUCCESS` or `FAILED`

## Steps Performed

1. **Data Cleaning & Preprocessing**
   - Removed non-numeric columns not needed for training
   - Label encoded categorical values (`sender_upi`, `receiver_upi`)
   - Converted `status` into binary (0: success, 1: fraud)

2. **Data Visualization**
   - Used bar plots and heatmaps to understand class imbalance and correlation

3. **Model Training**
   - Trained a Random Forest Classifier on 70% of the data
   - Evaluated on 30% test data

4. **Evaluation**
   - Classification report: Precision, recall, F1-score
   - Confusion matrix heatmap
   - Feature importance plot

## Requirements

Install the required libraries using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## How to Run

1. Open the `UPI_Fraud_Detection.ipynb` Jupyter notebook
2. Run all cells in order
3. View evaluation results and visualizations

## Results

The model achieves good classification performance on the test set. Feature importance analysis reveals that transaction amount and UPI IDs play a key role in identifying fraudulent behavior.

## Future Work

- Add anomaly detection for unseen fraud patterns
- Integrate with live transaction stream for real-time detection
- Build a web dashboard using Streamlit

## License

This project is for educational purposes only.
