## XGBoost model building lab

In this lab, I will construct my own XGBoost classification model. I will be presented with a business scenario and a dataset to use as I build on the skills and techniques I learned in the Decision Tree and Random Forest lessons. I will practice training, tuning, and evaluation an XGBoost model and compare its performance to previous models' to decide which model is best.

## Data Dictionary

This activity uses a dataset called `Invistico_Airline.csv`. It represents the details of customer feedback for Invistico Airlines (a fictional name).

The dataset contains:
- 23 columns of customer feedback, with each row representing one customer’s responses.
- Note that responses were given on a 0 to 5 scale, 0 meaning "not at all satisfied" and 5 meaning "very satisfied."

The dataset contains:
- 129,880 rows, each row is a different customer response 
- 23 columns

| Column name                  | Type | Description                                                                               |
|------------------------------|------|-------------------------------------------------------------------------------------------|
| Satisfaction                 | str  | Customer’s overall assessment of airline, either "satisfied" or "dissatisfied"             |
| Customer Type                | str  | Customer’s loyalty, "Loyal Customer" or "Disloyal Customer"                                |
| Age                          | int  | Customer’s age                                                                             |
| Type of Travel               | str  | Customer’s reason for travel, "business" or "personal"                                     |
| Class                        | str  | Customer’s purchased seat class, "Business," "Eco," or "Eco Plus"                          |
| Flight Distance              | int  | How far the flight traveled                                                               |
| Seat comfort                 | int  | Customer’s rating of seat comfort                                                         |
| Departure/Arrival time convenient | int | Customer’s rating of convenience for departure and arrival time                            |
| Food and drink               | int  | Customer’s rating of food and drink                                                        |
| Gate location                | int  | Customer’s rating of the convenience of the gate location                                  |
| Inflight wifi service        | int  | Customer’s rating of the inflight wifi/Internet service                                    |
| Inflight entertainment       | int  | Customer’s rating of inflight entertainment                                               |
| Online support               | int  | Customer’s rating of online support services of the airline                               |
| Ease of online booking       | int  | Customer’s rating of the ease of booking tickets online                                   |
| On-board service             | int  | Customer’s rating of service by airline personnel                                          |
| Leg room service             | int  | Customer’s rating of amount of legroom                                                    |
| Baggage handling             | int  | Customer’s rating of convenience or ease of baggage handling                              |
| Checkin service              | int  | Customer’s rating of check-in service by airline personnel                                |
| Cleanliness                  | int  | Customer’s rating of cleanliness of the airplane                                          |
| Online boarding              | int  | Customer’s rating of the online boarding process                                          |
| Departure Delay in Minutes   | int  | How long the departure delay was for the flight measured in minutes                       |
| Arrival Delay in Minutes     | int  | How long the arrival delay was for the flight measured in minutes                         |

*This data has been modified for the purposes of this exercise. Specifically, the Gender column was dropped. While acknowledgement of a gender spectrum varies across societies, many societies now understand that gender is not a binary and there is fluidity in the category across people and time, so creating categories that allow for that leads to more accurate data collection processes.

The dataset can be found on [Kaggle](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction).
