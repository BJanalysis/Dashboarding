# IPL 2024 Insights Dashboard

### Dashboard Link:  http://surl.li/tfkxp

## Problem Statement

This dashboard aims to provide comprehensive insights into IPL 2024, leveraging data science techniques. It delves into the performance metrics of players and teams over the past three years, facilitating strategic decision-making for fans, analysts, and teams. Through actionable insights and real-world scenarios, it empowers cricket enthusiasts to gain a deeper understanding of the game and make informed predictions for the upcoming season.

### Steps Followed

1. **Data Collection:** Gathered data from various sources including historical IPL records, player statistics, and team performance data.

2. **Data Analysis:** Utilized advanced data science techniques, including predictive modeling and trend analysis, to uncover hidden patterns and trends in the IPL data.

3. **Dashboard Design:** Designed an interactive and visually appealing dashboard using Power BI, allowing users to explore key metrics and insights with ease.

4. **Insightful Visualizations:** Created insightful visualizations such as charts, graphs, and tables to present primary and secondary insights derived from the data analysis.

5. **Predictive Analytics:** Employed predictive analytics to forecast top performers, qualifying teams, and the eventual winner and runner-up of IPL 2024.

6. **Additional Research:** Conducted additional research to enhance the predictive accuracy of the dashboard and provide valuable recommendations for IPL stakeholders.

7. **Engagement and Collaboration:** Encouraged engagement and collaboration among cricket enthusiasts and aspiring data scientists to share their predictions and insights on the platform.

Through this dashboard, users can gain a holistic view of IPL 2024, from individual player performance to team dynamics, enabling them to make data-driven decisions and elevate their cricketing experience. Join the conversation and be part of the IPL excitement!


### Key Metrics and Formulas

1. **Total Runs**
   - *Description:* Total number of runs scored by the batsman.
   - *Formula:* `Total Runs = SUM(fact_batting_summary[runs])`
   
2. **Total Innings Batted**
   - *Description:* Total number of innings a batsman got a chance to bat.
   - *Formula:* `Total Innings Batted = COUNT(fact_batting_summary[match_id])`
   
3. **Total Innings Dismissed**
   - *Description:* Number of innings batsman got out.
   - *Formula:* `Total Innings Dismissed = SUM(fact_batting_summary[out])`
   
4. **Batting Average**
   - *Description:* Average runs scored in an innings.
   - *Formula:* `Batting Avg = DIVIDE([Total Runs],[Total Innings Dismissed],0)`
   
5. **Total Balls Faced**
   - *Description:* Total number of balls faced by the batsman.
   - *Formula:* `Total Balls Faced = SUM(fact_batting_summary[balls])`
   
6. **Strike Rate**
   - *Description:* Number of runs scored per 100 balls.
   - *Formula:* `Strike Rate = DIVIDE([Total Runs],[Total Balls Faced],0)*100`
   
7. **Batting Position**
   - *Description:* Batting position of a player.
   - *Formula:* `Batting Position = ROUNDUP(AVERAGE(fact_batting_summary[batting_pos]),0)`
   
8. **Boundary %**
   - *Description:* Percentage of boundaries scored by the Batsman.
   - *Formula:* `Boundary % =  DIVIDE(SUM(fact_batting_summary[Boundary runs]),[Total Runs],0)`
   
9. **Average Balls Faced**
   - *Description:* Average balls faced by the batter in an innings.
   - *Formula:* `Average Balls Faced = AVERAGE(fact_batting_summary[balls])`
   
10. **Wickets**
    - *Description:* Total number of wickets taken by a bowler.
    - *Formula:* `Wickets = SUM(fact_bowling_summary[wickets])`
    
11. **Balls Bowled**
    - *Description:* Total number of balls bowled by the bowler.
    - *Formula:* `Balls Bowled = SUM(fact_bowling_summary[balls])`
    
12. **Runs Conceded**
    - *Description:* Total runs conceded by the bowler.
    - *Formula:* `Runs Conceded = SUM(fact_bowling_summary[runs])`
    
13. **Bowling Economy**
    - *Description:* Average number of runs conceded in an over.
    - *Formula:* `Bowling Economy = DIVIDE( [Runs Conceded], ([Balls Bowled]/6),0)`
    
14. **Bowling Strike Rate**
    - *Description:* Number of balls bowled per wicket.
    - *Formula:* `Bowling Strike Rate = DIVIDE([Balls Bowled], [Wickets],0)`
    
15. **Bowling Average**
    - *Description:* No. of runs allowed per wicket.
    - *Formula:* `Bowling Average = DIVIDE([Runs Conceded],[Wickets],0)`
    
16. **Total Innings Bowled**
    - *Description:* Total number of innings bowled by a bowler.
    - *Formula:* `Total Innings Bowled = DISTINCTCOUNT(fact_bowling_summary[match_id])`
    
17. **Dot Ball %**
    - *Description:* Percentage of dot balls bowled by a bowler.
    - *Formula:* `Dot Ball % = DIVIDE(SUM(fact_bowling_summary[zeros]), SUM(fact_bowling_summary[balls]),0)`
    
18. **Player Selection**
    - *Description:* To understand if a player is selected or not.
    - *Formula:* `Player Selection = IF(ISFILTERED(dim_player[name]), "1", "0")`
    
19. **Display Text**
    - *Description:* To display a text of no player is selected.
    - *Formula:* `Display Text = IF([Player Selection] = "1", " ", "Select Player(s) by clicking the player’s name to see their individual or combined strength.")`
    
20. **Color Callout Value**
    - *Description:* To display a value only when a player is selected.
    - *Formula:* `Color Callout Value = IF([Player Selection]="0", "#D0CF1D","#1D1D2E")`

These metrics and formulas provide valuable insights into the performance of players and teams in IPL 2024, facilitating informed decision-making and analysis.

[End of Document]
