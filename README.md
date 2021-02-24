# Exercise-Motion-Classification
## [Dacon] 운동 동작 분류 AI 경진대회
### 기간 : 2021.01.11 ~ 2021.02.22 17:59

private **69th** (0.81065) out of **336 teams** | public **90th** (0.86932) out of **336 teams**

대회 마감 4~5일전에 참여하여 deep한 insight를 내지 못 하고 다양한 시도를 해보지 못 한점이 아쉽지만 xgb model과 bayesian optimization을 사용하여 조금은 성능을 올릴 수 있었던 대회였다. 파생변수를 더 만들고, deep learning model과 ensemble model을 코드공유와 토론을 통해 많은 것을 느끼고 배울 수 있었다. 아쉽지만 대회가 끝난 후에 코드 리뷰와 부족한 점들을 채워나가면서 성능을 올리는 공부를 계속 해나가야겠다. 



|Model|notebook_name|parameters|logloss|submission_name|
|--|--|--|--|--|
|xgb|xgb_model|'eta':0.1,'objective':'multi:softprob','max_depth':3,'eval_metric':'mlogloss','seed':0,'lambda':2,'num_class':61, num_boost_round=100,early_stopping_rounds=100,verbose_eval = 50 |1.05432	|xgb_model|
|xgb|xgb_model|'eta':0.1,'objective':'multi:softprob','max_depth':3,'eval_metric':'mlogloss','seed':0,'lambda':2,'alpha':2,'num_class':61, num_boost_round=200,early_stopping_rounds=100,verbose_eval = 50|1.05341|xgb_model_ver1|
|xgb|xgb_model_ver2|'colsample_bytree': 0.9543751822448909,'eval_metric': 'mlogloss','gamma': 2.3765993313084093,'lambda_val': 4.823723573634545,'learning_rate': 0.0320405651413064,'max_delta_step': 4.17743472256279,'max_depth': 2,'min_child_weight': 7.118213702774423,'num_class': 61,'objective': 'multi:softprob','subsample': 0.9532572056575737,num_boost_round=200|0.96465|xgb_model_ver2|
|xgb|xgb_model_ver4+shift_data+add_feautres(mean,max,median,std,quantile_75,quantile_25)+bayesian_optimization|'colsample_bytree': 0.4,'gamma': 0.001,'lambda_val': 5.0,'learning_rate': 0.2,'max_delta_step': 10.0,'max_depth': 2.0,'min_child_weight': 0.0,'subsample': 1.0,'eval_metric' = 'mlogloss''objective' = 'multi:softprob''num_class' = 61|**0.86932**	|xgb_model_ver4|   
