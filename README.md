# GA_Clustering_Algorithm-with_Kmeans
GA-Clustering Algorithm 구현(with KMeans)
- file: GA_Clustering_Algorithm.ipynb

# GA Clustering 작동 과정
## 1. 랜덤하게 생성된 초기해 군(Population size)으로 시작
- 초기해 생성 시 KMeans로 생성한 해와 랜덤하게 생성한 해를 적절히 구성 가능?
- population_size 설정(KMeans에서 생성된 해를 일정 비율로 넣어보자!)

## 2. 초기해 평가
- Validation Function: **Intra-cluster distance**

## 3. Roulette wheel Selection

## 4. Crossover

## 5. Mutation
- mutation_prob 설정

## 6. 해 평가 후 Better Solution으로 업데이트

## 7. 종료조건까지 step 3 ~ 6 반복
- 종료조건 : max_generation, early stopping

# 실험 데이터셋(UCI example data)
- Iris Dataset
- Wine Dataset
- Glass Dataset
- Vowel Dataset
- Cloud Dataset

# KMeans 해를 포함한 GA Clustering 결과에 대한 해석

## [실험 전의 나의 생각]: KSA Clustering처럼 KMeans로 나온 좋은 해로 시작하면 더 좋지 않을까?

## [결과]: 더 좋은 해를 찾지 못하고 돌연변이에 의해 안 좋은 해로 나아감

## [결과에 대한 나의 생각]: SA와 GA의 최적해를 찾아가는 방식의 차이점이라고 생각함
- SA - 이웃해를 찾아나가면서 local search를 수행
- GA - local search를 수행하는 과정이 없고, crossover, mutation 과정이 KMeans 해에 일어나면서 더 안 좋은 해로 진행되게 됨.

--> GA에 Local search 기능을 추가한 Hybrid 버전이라면 더 좋은 해를 찾게 될 수 있지 않을까 생각한다.
