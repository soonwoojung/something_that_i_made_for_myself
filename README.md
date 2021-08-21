# something_that_i_made_for_myself

Check_Outlier.ipynb
```
1. IQR 상한,하한을 정함. (2분위수, 3분위수의 차이 * 2배)
2. IQR 경계를 넘는 값(아웃라이어)은 IQR 경계 값으로 치환함
3. 그리고나서 새로운 칼럼을 추가하고, 아웃라이어이면 1로 표시함. 아니면 0으로 표시함.
```

H2O_XGB_and_Optuna.ipynb
```
1. HyperParams 를 튜닝할때 유의점 : 너무 와이드한 서치 영역, 그리고 성능 향상에 그리 중요하지 않은 파라미터까지 처음부터 튜닝하려고 하면 비효율 적이다.
2. 차라리 중요한 몇개 파라미터를 튜닝 후, 그 다음 순차적으로 서치 영역과, 튜닝할 대상을 늘려가는게 더 효율적인 것으로 판단된다.
3. H2O 로 XGB 를 학습하면 장/단점이 존재한다. (체감상) Python 보다 빠른 것 같으나, 단점은 미지원되는 일부 기능(Custom Loss Function), Parameter(Scale Pos Weight) 들이 존재한다.
4. 그리고 원본 Params 와 명칭 자체가 다른 경우가 있으니 유의할 것.
```


CatB_and_Custom_L_Func.ipynb
```
1. CatBoost 의 입력값인 cat_features 는 자동으로 데이터 칼럼에서 카테고리형 칼럼을 선택하도록 했음
2. Custom Loss Function 예시를 넣어놨음 ( Focal Loss 에서 감명받은 부분이 반영됨.. 그런데 엄밀히 der2 ( hessian ) 값을 내가 쓴 것처럼 하면 안되긴 함. der1 의 미분 형태가 아님 )
```


