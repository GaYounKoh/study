# [Table of contents]
- [study](#study)
- [따릉이 스터디](#-------)
<!--->[잊지말고 블로그 repo에 추가하세요](#---------repo-------)<!--->
  * [학습순서](#----)
    + [따라하기](#----)
    + [시각화](#---)

# study
study
<br>

<!--->### 잊지말고 블로그 repo에 추가하세요<!--->


```python
from IPython.core.interactiveshell import InteractiveShell
InteractiveShell.ast_node_interactivity = "all"
```
<br>

[dacon page](https://dacon.io/competitions/official/235869/codeshare/4252?page=1&dtype=recent) <br>
<br>

# 따릉이 스터디
[따릉이 스터디](https://dacon.io/competitions/open/235576/overview/description) <br>

## 학습순서
0. [코드공유 > 따릉이 데이터를 활용한 데이터 분석 실습파일](https://dacon.io/competitions/open/235576/codeshare/1276?page=1&dtype=recent)<br>
0-1. [토크 > 따릉이 데이터를 활용한 데이터 분석 1 (EDA)](https://dacon.io/competitions/open/235576/talkboard/401060?page=1&dtype=recent) <br>
1. [코드공유 > 자전거 데이터 시각화](https://dacon.io/competitions/open/235576/codeshare/617?page=1&dtype=recent) <br>
2. [토크 > 따릉이 데이터를 활용한 데이터 분석 2 (전처리)](https://dacon.io/competitions/open/235576/talkboard/401061?page=1&dtype=recent) <br>
3. [토크 > 따릉이 데이터를 활용한 데이터 분석 3 (모델링)](https://dacon.io/competitions/open/235576/talkboard/401062?page=1&dtype=recent) <br>
4. [코드공유 > [제주TP] 따릉이 모델 평가프로그램](https://dacon.io/competitions/open/235576/codeshare/1545?page=1&dtype=recent) <br>

### 따라하기
[코드공유 > [제주TP] 따릉이 공유](https://dacon.io/competitions/open/235576/codeshare/1535?page=1&dtype=recent) <br>
<br>


### 시각화
[matplotlib tutorial](https://wikidocs.net/book/5011) <br>
[데이터 시각화 seaborn](https://wikidocs.net/86290) <br>
[데이터 시각화 예제](https://m.blog.naver.com/icbanq/222056484058) <br>
[데이터 핸들링 matplotlib](https://cool24151.tistory.com/16) <br>
[matplotlib에서 그림판 크기를 변경하는 방법](https://www.delftstack.com/ko/howto/matplotlib/how-to-change-the-figure-size-in-matplotlib/) <br>

### 한글깨짐
[VSCode 한글 깨짐 현상 해결](https://apple-py.tistory.com/entry/%EC%9B%8C%EB%93%9C-%ED%81%B4%EB%9D%BC%EC%9A%B0%EB%93%9C%EB%A5%BC-%ED%99%9C%EC%9A%A9%ED%95%9C-%EB%A6%AC%EB%B7%B0-%EB%8D%B0%EC%9D%B4%ED%84%B0-%EC%8B%9C%EA%B0%81%ED%99%94-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-%EC%A0%9C-1%ED%8E%B8-Visual-Studio-Code%EC%97%90%EC%84%9C-Jupyter-Notebook-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0) <br>
[한글깨짐 현상 해결](https://itisik.tistory.com/114)

### 하이퍼파라미터 튜닝
[머신 러닝 - 하이퍼 파라미터 튜닝](https://velog.io/@skarb4788/%EB%A8%B8%EC%8B%A0-%EB%9F%AC%EB%8B%9D-%ED%95%98%EC%9D%B4%ED%8D%BC-%ED%8C%8C%EB%9D%BC%EB%AF%B8%ED%84%B0-%ED%8A%9C%EB%8B%9D) <br>
[머신러닝 - 13. 파라미터(Parameter)와 하이퍼 파라미터(Hyper parameter)](https://bkshin.tistory.com/entry/%EB%A8%B8%EC%8B%A0%EB%9F%AC%EB%8B%9D-13-%ED%8C%8C%EB%9D%BC%EB%AF%B8%ED%84%B0Parameter%EC%99%80-%ED%95%98%EC%9D%B4%ED%8D%BC-%ED%8C%8C%EB%9D%BC%EB%AF%B8%ED%84%B0Hyper-parameter) <br>
[하이퍼 파라미터 종류](http://blog.skby.net/%ED%95%98%EC%9D%B4%ED%8D%BC%ED%8C%8C%EB%9D%BC%EB%AF%B8%ED%84%B0-hyperparameter/) <br>
[[ML] Feature Selection (Filter Method & Wrapper Method & Embedded Method)](https://wooono.tistory.com/249) - feature selection, feature engineering, feature extraction 비교<br>

## 220703 타이타닉, rocauc 점수
예측 인풋에는 수치형만! <br>

1st_submission(X_train에서 ['Ticket', 'Cabin', 'Embarked'] 제외하고 학습 진행.) : 0.65194 <br>

2nd_submission(1st_try에 이어서, 'Embarked'의 S, C, Q를 각각 1,2,3으로 맵핑하고 예측) : 0.678067186 <br>

```python
# mapping code
test['Embarked'] = test['Embarked'].map({'S':1, 'C':2, 'Q':3})
```

--> feature 늘린 게 결과 더 좋았음.

[가연 추가 과제]
XGBoost 돌리기 (앙상블 기법에 대한 공부)
상관관계로 증명

[유진]
이상치 제거 못함, 결측치 최빈값으로
전처리 정규화
value가 세세하게 나와있는 경우 상관관계가 더 높지 않았나

[정윤]
성별 중요

[예진]
결측 평균값으로
predict 대신 predict_proba

proba 예측 확률로 나옴, 회귀는 연속값으로 나올 것
오차중 가장 낮게..?
proba는 공모전에서 못쓸 것. (proba 대신 regressor를 쓰면 되지 않을까?)
<br>
<br>

3rd_submission(2nd_try에 이어서, 알고리즘으로 xgboost 선택): 0.6762658228 <br>

4th_submission(2nd_try에 이어서, 정윤 feature로 feature 대폭 줄임): 0.7124634859
정윤피쳐: 'Pclass', 'Sex'

[형준]
튜닝 optuna로 <br>
[형준 참고](https://velog.io/@lsmmay322/%ED%83%80%EC%9D%B4%ED%83%80%EB%8B%89-%EC%A0%9C%EB%8C%80%EB%A1%9C-%EB%B6%84%EC%84%9D%ED%95%B4%EB%B3%B4%EA%B8%B0#%EC%83%81%EA%B4%80%EA%B3%84%EC%88%98correlation) <br>

random search 속도 문제

5th_submission(4th_try에 이어서, 피쳐 바꿔서): 0.6474196689
'Sex', 'Age', 'Fare'

6th_submission(5th_try에 이어서, 피쳐 추가): 0.6659688413
'Pclass', 'Sex', 'Age', 'Fare'

💛그냥 모델링시 가장우수💛 7th_submission(6th_try에 이어서, 피쳐 변경): 0.7304771178
'Sex', 'Fare'

8th_submission(7th_try에 이어서, 피쳐 추가): 0.7197419669	
'Pclass', 'Sex', 'Fare'

💛지금까지 중 가장우수💛 9th_submission(7th_try에 이어서, grid search cv): 0.7362463486
best_parameters : learning_rate = 0.01, n_estimators = 500
[사실상 하이퍼파라미터튜닝은 한물 간 기법이라고 한다.](https://koreapy.tistory.com/940) <br>

010th_submission은 9th에 이어서, feature selection을 진행했는데... feature가 뭐가 뽑혔는지 알 수 없어서 X_test 그냥 9th와 똑같이 집어 넣었더니 결과 이전과 동일.

값을 비교해 확인해보니 9th try와 같은 feature 나옴. 저게 최대 점수인듯.
feature selection 결과 뽑힌 feature 확인하는 방법 좀....


011th_submission(010th try에 이어서, .feature_importance_로 나오는 피쳐, 009th try에서의 hyper parameter 사용.): 0.5721518987
'Fare', 'Age'

💔똥망💔 012th_submission(010th try에 이어서, .feature_importance_로 나오는 피쳐, 011th try에서의 새로운 feature에 맞춘 새로운 hyper parameter 사용, 결과 좋지 않을 것으로 예상.): 0.5625365141	
best_parameters : learning_rate = 0.05, n_estimators = 100

feature selection과 feature_importance_ 결과가 다름.
[Feature importances with a forest of trees](https://scikit-learn.org/stable/auto_examples/ensemble/plot_forest_importances.html#sphx-glr-auto-examples-ensemble-plot-forest-importances-py): example on synthetic data showing the recovery of the actually meaningful features.

```python
# 이런 식으로도 사용함.
clf = Pipeline([
  ('feature_selection', SelectFromModel(LinearSVC(penalty="l1"))),
  ('classification', RandomForestClassifier())
])
clf.fit(X, y)
```

[feature selection의 장점 외](https://subinium.github.io/feature-selection/) <br>
```
SelectFromModel
decision tree 기반 알고리즘에서 피처를 뽑아오는 방법입니다.
RandomForest나 LightGBM 등
```

[grid search 시 참고한 자료](https://blog.naver.com/PostView.nhn?isHttpsRedirect=true&blogId=healingview&logNo=221244848751&parentCategoryNo=&categoryNo=&viewDate=&isShowPopularPosts=false&from=postView)