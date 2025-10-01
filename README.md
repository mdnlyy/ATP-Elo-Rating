# Elo Rating for ATP Matches 🎾

##  Objective
Analyze ATP match data from the past decade and build an **Elo rating system** to estimate player strength and predict match outcomes.  
The project also applies a **logistic regression model** to test how Elo ratings and match context (surface, Grand Slam status) explain win probabilities.

---

## Datasets Used
- ATP match records (2014–2024, one CSV per year)  
- ATP matches from Jan–Sep 2025  
- Player rankings (2010–2024)  
- Player information for all professional ATP players (1968–2024)  

---

##  Project Structure
1. **Data loading & cleaning**  
2. **Identifying top-20 players (2020–2024)**  
3. **Exploratory analysis**  
   - Player performance across surfaces  
   - Yearly performance comparison  
   - Head-to-head weaknesses (e.g., Carlos Alcaraz vs top-20 in 2023–2024)  
4. **Elo rating system**  
   - Custom implementation (player Elo ratings updated after each match)  
5. **Machine learning model**  
   - Logistic Regression using Elo difference, surface, and Grand Slam flag  
   - Evaluated with accuracy, LogLoss, and Brier Score  
6. **Case study**  
   - Predicted probability for Djokovic vs Alcaraz  

---

## Key Results
- **Accuracy**: 73.6%  
- **Log Loss**: 0.526  
- **Brier Score**: 0.175  

**Case Study**:  
The model predicts that Novak Djokovic would win against Carlos Alcaraz with a probability of **58%**.  
*(Note: model trained on 2020–2024 matches, so recent ATP trends may not be fully captured.)*

---

## 🛠 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/mdnlyy/ATP-Elo-Rating.git
   cd ATP-Elo-Rating
2. Install dependencies:
   pip install -r requirements.txt
3. Open the notebook:
   jupyter notebook atp_elo_notebook.ipynb


## Limitations
- Dataset limited to 2020–2024 for Elo training → may not reflect latest player form.
- Elo system does not account for injuries, scheduling, or psychological factors.
- Only simple features used (Elo difference, surface, Slam flag).

## Author
Developed as part of a data science portfolio project.

## Acknowledgements
- ATP match, ranking, and player data sourced from [Jeff Sackmann's Tennis ATP repository](https://github.com/JeffSackmann/tennis_atp).  
  Please cite Jeff Sackmann if you use this data in your own projects. 