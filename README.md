
Goal: To build a model to predict the severity of road accident

Steps:
1) Data preprocessing
2) Model building
3) parameter tuning
4) model evaluation

1) Data preprocessing steps: <br>
EDA:<br>
    1)Replacing Null values<br>
    2)Attribute selection for categorical values based on mean aggregation and annova test<br>
    3)Handling Outliers (for numeric data)<br>
    4)Attribute selection for numeric data columns<br>
    5)Encoding and Normalization<br>
    6)Data spliting into train 75%,val 15%,test 10%<br>

2) model building: <br>
-> Randomforest regressor<br>
-> XGboost regrssor<br>
-> ANN nueral network for regression task<br>

3) parameters are tuned based on validation accuracy 
(Could use gridsearchcv, but as the data is huge, as it will be computationally expensive)<br>

4) Final model evaluation <br>

___________________________________________________________________________________________
| Model                  | Validation Loss (MSE) | Test Loss (MSE) | r2_score (val. data) |
|------------------------|-----------------------|-----------------|----------------------|
| Random Forest          | 0.115                 | 0.114           | 0.506                |
| XGBoost Regressor      | 0.127                 | 0.126           | 0.51                 | 
| ANN                    | 0.17                  | 0.17            |                      |
-------------------------------------------------------------------------------------------

loom link video: https://www.loom.com/share/26fe23fe84c64902935db39fbde7e165?sid=f425f04d-0352-4571-90c3-46b5392a6391
(The models are not explained clear in the demo video as the video recording time is only 5min)

Research remcommendation:

-> We can also consider speed of the vehicles for accident severity <br>
-> Even though some areas like junctions or cross signals have more chance of accidents, there are some scenarios <br>
where the accidents can happend like near the crowded places, No zebra cross areas, or Hospital areas where there is hight inflow and outflow of public<br>
-> And it didn't include the snowfall, in some areas snow fall may contribute to the accident severity<br>
-> and visiblity of road signs too, snow fall may block the signs sometimes<br>
-> Accidents also can happen in forest areas where the animals sometimes suddently showup on the road<br>