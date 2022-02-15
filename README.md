[OP.GG](https://www.op.gg/) had complete data for League of Legends, which can be used to build ML models.

## Approach
In this project, I used Korean region top 2000 players' last 20 games data.

In each game, every lane (5 lanes) had five types of data:
+ Win Rate
+ Lane Kill Rate
+ KDA
+ Kill Participation
+ Damage Dealt to Champions

<p style="text-align: left;">
<img src="images/data_sources.png" alt="drawing" width="400"/>
</p>

As a result, there are 23 types of in each game. (Jungle position had no lane kill rate, while support position had no damage dealt)

Besides, the output Y is the result (0: red side win, 1: blue side win)

The dataset contains 19941 rows, 80% for training, 10% for validating, 10% for testing

<p style="text-align: left;">
<img src="images/data_preview.png" alt="drawing" width="400"/>
<br>
<img src="images/data_splitting.png" alt="drawing" width="400"/>
</p>

## Result
AUC score: 0.61

True Win: 602<br>
True Lose: 550<br>
False Win: 425<br>
False Lose: 417<br>
Test score: 0.58

<p style="text-align: left;">
<img src="images/result.png" alt="drawing" width="400"/>
</p>
