# ML_lec_03: Linear Regression의 cost최소화 알고리즘의 원리 설명 

## (1) gradient descent algorithm

![image](https://user-images.githubusercontent.com/28600272/43850284-813f903e-9b72-11e8-9d1f-04ed906a4052.png)

- cost function = cost가 최소화되는 점을 찾는 것!
  - 이 점을 기계적으로 찾아내는 것이 목적임 
- 이를 위해 사용되는 알고리즘이 gradient descent algorithm
  - gradient = 경사
  - descent = 내려감 
- 즉, 경사를 따라 내려가는 알고리즘 
- 주어진 코스트 펑션을 미니마이즈하는데 사용됨 
- 여러개의 값들이 있을 때 (w1,....wn) 코스트를 최소화할 수 있음 


## (2) 알고리즘 원리 

- 어떻게 최소값을 찾을 것인가? 
  - 산에 올랐다고 생각해보자. 계속 내리막길을 따라 내려가다보면 경사도 0에 도착. 
- 아무 값에서 시작할 수 있음 
- w를 조금씩 바꾸면서 cost(w, b)를 줄일 수 있음  (cost = 경사도)


## (3) 알고리즘 Formal Definition

![image](https://user-images.githubusercontent.com/28600272/43850789-df951342-9b73-11e8-925b-b8c0b3d26e31.png)

- 주어진 그래프에서 경사도를 찾아야 하기에 미분이 필요 
- 현재의 w - ( a(running rate) * cost함수를 미분한 것 )
  - 기울기가 -라면 더 w를 더 작은 값으로 움직이겠다 
  - 기울기가 +라면 더 w를 더 큰 값으로 움직이겠다
- 여러 번 실행시키면서 w가 계속 변화함 
- 이 수식을 기계적으로 적용시키면 바로 cost function을 최소화하는 w를 구할 수 있음 > linear reg의 핵심인 학습과정을 통해 모델을 만듦 

## (4) convex function

- 만약 cost function이 3차원이라면
  - 처음 시작점에 따라서 다른 결과가 나올 수 있음 > 즉 gda이 답을 찾아주지 못함 
- convex인 경우에는 어느점에서 시작해도 항상 도착하는 점이 우리가 원하는 지점
  - 이러한 경우에는 gda이 항상 답을 찾아줌 
```
cost function의 모양이 convex인지 확인 필요! 필수!
```
