# 자전거 수요량 예측
### 요약
자전거 대여량 데이터를 통해 대여 수요를 예측해보았다. 예측의 정확도를 높이기 위해 아래의 순서로 시도를 하고 각각의 RMSE, MAE 를 구했다.

1. 시간 컬럼만 추가
2. 연, 월 컬럼 추가
3. One-Hot Encoding
4. LGBM Regressor
5. 1시부터 5시는 5시로 통합
6. 0 미만의 예측값은 0으로 변환

1번부터 6번까지의 변화를 보면<p>
- RMSE: 147.217 -> 139.978 -> 104.044 -> 49.573 -> 48.005 -> 47.975
- MAE: 108.096 -> 105.029 -> 75.559 -> 31.859 -> 31.141 -> 31.050
<p>순으로 나타났다.
<p>다만 2012년 이후의 미래를 예측해야한다고 가정할 때 연도 데이터는 사용할 수 없으므로 연도 정보 없이 점수를 구해보면

- RMSE: 69.024, MAE: 47.638
<p>으로 나온다.
