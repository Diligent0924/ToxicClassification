# 독성 문장 판별을 위한 자연어처리 모델링

## 개요
빅데이터 분석기사 취득 후 조금 더 새로운 모델링을 하기 위하여 Kaggle Data를 찾는 중 독성 문장에 따른 자연어처리 분석 Competition을 확인하여 진행

## 내용
* DataSet : Training DataSet, Validation DataSet ( 8000개 ) / Test DataSet ( 3000개 )
* Modeling : BERT (bert-base-uncased)
* HyperParameter
  * num_train_epochs= 5           
  * per_device_train_batch_size= 16
  * per_device_eval_batch_size= 16
  * warmup_steps= 5000               
  * weight_decay= 0.01              
  * logging_dir='./logs'         
  * report_to = 'wandb'
  * run_name="toxic model"
  * evaluation_strategy = 'epoch'
* metrics : 'glue','mrpc'

# 결과값
![image](https://user-images.githubusercontent.com/62194486/220803605-986b0649-81dd-4c8b-bf72-66fa020b7e92.png)
