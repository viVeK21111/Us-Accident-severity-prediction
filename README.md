
Goal: To build a model to predict the severity of road accident

Steps:
1) Data preprocessing
2) Model building
3) parameter tuning
4) model evaluation

1) Data preprocessing steps:
EDA:1)Replacing Null values
    2)Attribute selection for categorical values based on mean aggregation and annova test
    3)Handling Outliers (for numeric data)
    4)Attribute selection for numeric data columns
    5)Encoding and Normalization
    6)Data spliting into train 75%,val 15%,test 10%

2) model building:
-> Randomforest regressor
-> XGboost regrssor
-> ANN nueral network for regression task

3) parameters are tuned based on validation accuracy 
(Could use gridsearchcv, but as the data is huge, as it will be computationally expensive)

4) Final model evaluation
-> Random forest (mse)     val_loss:0.115    test_loss:0.114
-> XGboost regressor (mse) val_loss:0.127    test_loss:0.126
-> ANN (mse)               val_loss:0.17     test_loss: 0.17

loom link video: https://www.loom.com/share/26fe23fe84c64902935db39fbde7e165?sid=f425f04d-0352-4571-90c3-46b5392a6391
(The models are not explained clear in the demo video as the video recording time is only 5min)

Research remcommendation:

-> We can also consider speed of the vehicles for accident severity
-> Even though some areas like junctions or cross signals have more chance of accidents, there are some scenarios
where the accidents can happend like near the crowded places, No zebra cross areas, or Hospital areas where there is hight inflow and outflow of public
-> And it didn't include the snowfall, in some areas snow fall may contribute to the accident severity
-> and visiblity of road signs too, snow fall may block the signs sometimes
-> Accidents also can happen in forest areas where the animals sometimes suddently showup on the road