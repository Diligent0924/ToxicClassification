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

# Epoch 그래프
![image](https://user-images.githubusercontent.com/62194486/220803605-986b0649-81dd-4c8b-bf72-66fa020b7e92.png)


# 결과값
* 약 80% 정확도

# 후기
독학으로 자연어처리를 진행하였는데 새로운 모델을 배울 수 있어서 많은 도움이 되었다. 다만, BERT 모델 자체를 이해하기는 너무 어려웠으며 Tokenizing과 Attention에 대한 개념만 조금 이해를 한 정도였다. 이러한 모델링이 있다는 것에 대한 경험을 했다는 것에 만족해야할 것 같으며 만약 깊게 들어가고자 한다면 석/박사를 연계하여 진행해야할 것 같다.
