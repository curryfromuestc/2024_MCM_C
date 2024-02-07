# 2024_MCM_C_UESTC
The code and the processed datasets of 2024_MCM_UESTC  
## Code  
## Datasets  
## Summary  
In tennis matches, players can establish momentum through successful key events, gaining a sustained advantage. We separately develop models for player performance and momentum,allowing us to visualize the fluctuations in the game and provide advice to players.
To capture the changes in player performance as points occur and predict them over time, we build a player performance prediction model based on CNN-LSTM. Quantitative indicators for player performance, denoted as 𝑃, are obtained from three dimensions: scoring, psychological state, and fatigue level. Combining CNN and LSTM, we predict player performance. Testing the model on Alcaraz and Djokovic’s final match data, we use the difference in 𝑃 between the two
players to reflect their relative performance and visualize the match flow.
Next, we develop a player momentum model based on a multi-layer perceptron to quantify player momentum. Key events influencing the outcome are selected as input features, and through forward and backward propagation, we obtain momentum reflecting the probability of winning the subsequent points. Then we create a Pearson chi-squared test model to investigate whether player performance and scores are related to momentum rather than being entirely random. The conclusion is that we can confidently reject the coach’s statement at a 95% confidence level. Additionally, we introduce Kendall’s Tau hypothesis test, Spearman correlation coefficient hypothesis test, and permutation test to further validate our findings.
Subsequently, a match fluctuation model based on momentum changes is established. Using obtained momentum, we identify turning points in player advantage: when a player’s momentum transitions from less than 0.5 to greater than 0.5, or vice versa, it indicates an exchange in the player’s advantage and disadvantage situations. Testing on Alcaraz and Djokovic’s final match dataset yields an accuracy of 0.8042, demonstrating the effectiveness of the player momentum and
match fluctuation model. Furthermore, a Spearman correlation test on momentum and selected event indicators concludes that being server and gaining a turning advantage have the most apparent correlation, while the occurrence of unforced errors has the most noticeable correlation with being
in a disadvantaged turning position.
In the next step, we train and test the established player momentum and match fluctuation models on the 2023 US Open women’s singles and the 2017-2018 England Premier League dataset.
Particularly, adjustments are made to momentum considering the characteristics of football matches.
The final accuracy is 0.8276 and 0.7209, respectively, indicating strong generalization capabilities across genders, court surfaces, and sports events.
Finally, we provide a memorandum for coaches, elucidating the role of momentum and offering advice based on these findings.
