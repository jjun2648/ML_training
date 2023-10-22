# 군집화 실습 과제
### 요약
초등 학생의 국어, 영어, 수학, 과학, 사회, 역사 시험 점수를 통해 수준별 군집화를 진행하였다. 각각의 과제에 대해 실습한 내용은 아래와 같다.
1. 과제 1
    - 전체 데이터 사용
    - PCA 진행 / 미진행 나눠서 GMM 으로 군집화
    - histplot과 kdeplot으로 분포 시각화<p>
2. 과제 2
    - 국어와 수학 과목 데이터만 사용
    - K-means 이용해 5개 군집 만들기
    - K-means 이용해 4개의 군집을 만든 것과 비교
    - GMM으로 시각화해보기
    <p>

### 결과
1. 과제 1번 시각화 자료의 kde plot을 보면 PCA를 실행한 경우 좀 더 정규분포의 형태를 띄는 것으로 보인다. 다만 수치가 아닌 시각화 자료만으로는 정확하게 알 수는 없다. 반면 군집 간의 데이터 수는 PCA를 적용하지 않은 쪽이 조금 더 고르게 나뉘었는데 PCA에 의한 것인지 데이터 형태에 의한 것인지는 여러가지 경우를 실험해봐야 알 수 있을 것 같다.<p>
- PCA 미적용
<img src="https://github.com/jjun2648/ML_training/blob/main/%EA%B5%B0%EC%A7%91%ED%99%94%20%EC%8B%A4%EC%8A%B5%20%EA%B3%BC%EC%A0%9C/images/non_pca.png">

- PCA 적용
<img src="https://github.com/jjun2648/ML_training/blob/main/%EA%B5%B0%EC%A7%91%ED%99%94%20%EC%8B%A4%EC%8A%B5%20%EA%B3%BC%EC%A0%9C/images/pca.png">

---
2. 과제 2번의 데이터는 국어와 수학의 2개 축으로 되어있기 때문에 굳이 군집을 나눈다면 국어와 수학 점수의 높고 낮음에 따라 4개의 군집으로 나누는 것이 의미가 있는 군집화일 것이다. 이 상황에서 5개의 군집으로 나누라고 했을 때 K-means는 어느정도 비율을 맞춰가며 5개의 군집을 만든 반면, gmm은 하나의 군집을 버리다시피 하고 의미있는 4개의 군집을 형성했다. 다만 이 경우에도 데이터 형태와 우연이 겹친 것인지는 몇 가지 경우를 시험해봐야 알 수 있을 것이다.

- 5개 그룹 kmeans clustering
<img src="https://github.com/jjun2648/ML_training/blob/main/%EA%B5%B0%EC%A7%91%ED%99%94%20%EC%8B%A4%EC%8A%B5%20%EA%B3%BC%EC%A0%9C/images/kmeans_5.png">

- 4개 그룹 kmeans clustering
<img src="https://github.com/jjun2648/ML_training/blob/main/%EA%B5%B0%EC%A7%91%ED%99%94%20%EC%8B%A4%EC%8A%B5%20%EA%B3%BC%EC%A0%9C/images/kmeans_4.png">

- GMM
<img src="https://github.com/jjun2648/ML_training/blob/main/%EA%B5%B0%EC%A7%91%ED%99%94%20%EC%8B%A4%EC%8A%B5%20%EA%B3%BC%EC%A0%9C/images/GMM.png">

