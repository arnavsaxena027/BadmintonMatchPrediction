# 🏸 Badminton Match Outcome Prediction

This project predicts the winner of a badminton match between two players using match statistics such as ranks and previous wins. It uses a simple rule-based approach to classify outcomes based on engineered features.

---

## 📁 Dataset

- **Source**: `match_data.csv` (manually compiled)
- **Features Used**:
  - `Player 1 Name`
  - `Player 2 Name`
  - `Player 1 Rank`, `Player 2 Rank`
  - `Player 1 Wins`, `Player 2 Wins`
  - `Player 1 Total Matches`, `Player 2 Total Matches`
- **Target**:
  - `Winner`: Categorical outcome based on higher predicted win probability

---

## 🧠 Methodology

- Data loaded and cleaned using `pandas`
- Created additional features:
  - `Rank Difference` = Player 1 Rank - Player 2 Rank
  - `Win Rate 1` = Player 1 Wins / Total Matches
  - `Win Rate 2` = Player 2 Wins / Total Matches
  - `Win Rate Difference` = Win Rate 1 - Win Rate 2
- Winner was predicted as **Player 1** if `Win Rate 1 > Win Rate 2`, else **Player 2**

---

## 📈 Results

- This is a **rule-based predictor**, not a trained ML model
- Predictions are printed for each row, but no accuracy metric is computed
- Visualization used: Matplotlib bar plot to compare Player 1 and Player 2 win rates

---

## 📦 Requirements

Install required Python packages:

```bash
pip install pandas numpy matplotlib

# Clone the repository
git clone https://github.com/arnavsaxena027/BadmintonMatchPrediction.git
cd BadmintonMatchPrediction

# Open the notebook
jupyter notebook badminton_prediction.ipynb

