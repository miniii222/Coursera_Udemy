# Recommender System 강의 정리

## Probelm Formulation
#### - 기본적인 아이디어는 유저가 아직 평가하지 않은 영화를 몇 점이라고 평가할 것인가를 예측
- 영화 예시를 사용.
- n_u : number of users
- n_m : number of movies
- r(i,j) : user j가 movie i를 평가했으면 1, 아니면 0
- y(i,j) : 평가한 점수 (only r(i,j)=1)
- 데이터 형태 : n_m X n_u


## Content-based recommendations
#### - 기본 가정 : 각 영화의 특징을 나타내는 degree가 feature로 있어야 함
- romanticness, actionness 의 degree를 나타내는 feature x1, x2가 각 영화별로 있음
- i번쨰 영화 에 대하여 X^(i) = [1, x1, x2]^T. 이때, 1은 intercept 항
- j번째 유저에 대하여 theta^(j) = [0, a, b]^T. 이때, 0은 intercept 항. 여기서 a,b가 정확히 뭔지 잘 모르겠음
- predicted rating for user j, movie i = [theta^(j)^T , X^(i)] (내적)
- 모든 값들에 대해 loss를 줄이는 방식으로 예측

## Collaborative filtering
#### - 기본 가정 : 각 영화의 특징을 나타내는 feature 대신, user들이 말해준 점수가 있어야 함
- x1,x2가 주어졌던 상황 대신, user들의 선호도라고 할 수 있는 theta값들이 주어짐
- x1,x2와 같은 영화의 특징을 반영한 feature를 뽑아내는 것이 소모적.
- 주어진 theta값을 가지고 x1,x2를 추정하고, 추정된 값으로 다시 theta값을 추정하고 반복
- loss 값 역시, theta와 x들을 동시에 최소화하는 방향


