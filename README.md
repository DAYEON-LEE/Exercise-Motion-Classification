# Exercise-Motion-Classification
## [Dacon] 운동 동작 분류 AI 경진대회
### 기간 : 2021.01.11 ~ 2021.02.22 17:59

|Model|notebook_name|parameters|logloss|submission_name|
|--|--|--|--|--|
|xgb|xgb_model|'eta':0.1,'objective':'multi:softprob','max_depth':3,'eval_metric':'mlogloss','seed':0,'lambda':2,'num_class':61, num_boost_round=100,nfold=5,early_stopping_rounds=100,verbose_eval = 50 |1.05432	|xgb_model|
|xgb|xgb_model|'eta':0.1,'objective':'multi:softprob','max_depth':3,'eval_metric':'mlogloss','seed':0,'lambda':2,'alpha':2,'num_class':61, num_boost_round=200,nfold=3,early_stopping_rounds=100,verbose_eval = 50|1.05341|xgb_model_ver1|
