# Exercise-Motion-Classification
## [Dacon] 운동 동작 분류 AI 경진대회
### 기간 : 2021.01.11 ~ 2021.02.22 17:59

|Model|notebook_name|parameters|logloss|submission_name|
|--|--|--|--|--|
|xgb|xgb_model|'eta':0.1,'objective':'multi:softprob','max_depth':3,'eval_metric':'mlogloss','seed':0,'lambda':2,'num_class':61, num_boost_round=100,early_stopping_rounds=100,verbose_eval = 50 |1.05432	|xgb_model|
|xgb|xgb_model|'eta':0.1,'objective':'multi:softprob','max_depth':3,'eval_metric':'mlogloss','seed':0,'lambda':2,'alpha':2,'num_class':61, num_boost_round=200,early_stopping_rounds=100,verbose_eval = 50|1.05341|xgb_model_ver1|
|xgb|xgb_model_ver2|'colsample_bytree': 0.9543751822448909,'eval_metric': 'mlogloss','gamma': 2.3765993313084093,'lambda_val': 4.823723573634545,'learning_rate': 0.0320405651413064,'max_delta_step': 4.17743472256279,'max_depth': 2,'min_child_weight': 7.118213702774423,'num_class': 61,'objective': 'multi:softprob','subsample': 0.9532572056575737,num_boost_round=200|0.96465|xgb_model_ver2|
