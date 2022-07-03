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
1st_submission(X_train에서 ['Ticket', 'Cabin', 'Embarked'] 제외하고 학습 진행.) : 0.65194 <br>

2nd_submission(1st_try에 이어서, 'Embarked'의 S, C, Q를 각각 1,2,3으로 끼워넣고 예측) : 0.678067186 <br>

feature 늘린 게 결과 더 좋았음.