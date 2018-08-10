# ML_lec_05_1: logistic classification의 가설함수 정의 


### regression
- 코스트를 최소화하는 웨이트를 찾아내는 것 

### classification
- Classficaiton 알고리즘 중 정확도가 높은 알고리즘 
- 뉴럴네트워크와 딥러닝에 굉장히 중요한 개념 

## (1) binary classification

- spam detection / facebook feed / credit card fraudulent transaction detection 
- 0,1 encoding 

### 예: pass/fail based on study hours
- linear regression 으로 할 수 있을까? 

- classification은 반드시 값이 0,1 사이의 값이 나와야함
- 하지만 리그레션은 1보다 크거나 0보다 작거나 등의 값을 가질 수 있음 
  - 우리가 가지고 있는 데이터로 학습을 한다고 가정 (w=0.5)
  - x가 1,2,4,5,6,11로 모델을 학습시키고 y가 0~1사이 값이 나왔다고 가정
  - 하지만 input이 100일때 y값이 너무 커짐 = 50

- 리니어 리그레션은 간단해서 좋긴한데 문제가 좀 있네...
- 그럼 y를 0과 1 사이의 값으로 압축을 시켜주는 함수가 없을까?! 
  - **=simgmoid function** or **logistic function**
  
## (2) logistic classification hypothesis 
![image](https://user-images.githubusercontent.com/28600272/43935692-194aded8-9c90-11e8-966b-d34da5bba6af.png)


  
# ML_lec_05_2: logistic refression의 cost 함수 설명 

![image](https://user-images.githubusercontent.com/28600272/43935860-d7528994-9c90-11e8-89f9-d0d1e7cbb449.png)

- 구불구불하게 함수가 나오면 경사하강법에서 시작점이 어디인지에 따라서 최저점(local minimum)이 달라질 수 있음
- 하지만 우리가 찾고자하는 건 global minimum 
  - 따라서 이러한 형태의 그래프는 사용할 수 없음
  - linear에서 hypothesis도 바꿨기에 cost function도 바꿔야함 


