<center><h1>**종합설계 제안서**</h1></center>
<div style = "text-align:right; font-size: 13px;margin-bottom:40px;">강추 조 : 한정(컴공, 12114497), 이강호(컴공, 12142380)</div>

## 주제

<h5>최종목표 : **다양한 사용자 환경을 만족시키는 시간표 웹 제작 및 사용자 맞춤 수업 추천 시스템 구축**</h5>
* 시간표를 웹, 모바일 웹 모두에서 쉽게 작성할 수 있게 도와준다.
* 추천을 하는 것 : 교수님의 특정강의
    * 개인의 평가를 받아 이 평가를 기반으로 추천을 해주게 됩니다.
    * 평가 점수를 예측하고 개인과 유사한 집단을 찾아 개인의 점수를 예측합니다.
    * 여러 알고리즘을 적용해 보고 MAE(Mean Absolute Error)를 기준으로 추천 방식을 지속적으로 개선합니다.
        * 데이터의 특성에 따라 여러가지 알고리즘을 선택해 보고 더 나아가 저희만에 추천 알고리즘을 만드는 것을 목표로 하고 있습니다.
        * MAE : 예측 점수와 실제 점수의 차이를 측정하여 평균을 낸다. 이를 통해 해당 알고리즘의 정확성과 가중치를 판단 할 수 있습니다.
    * 이를 통해 추천의 만족도를 높일 수 있을 것입니다.
* UI prototype
    <div>
        <img src = '/img/mockmain.png' width='400' alt = 'prototype_ex1'/>
        <span>*메인 화면입니다.*</span>
        <img src = '/img/mockinfo.png' width='400' alt = 'prototype_ex2'/>
        <span>*개인정보 화면입니다*</span>
        <img src = '/img/mockrecommend.png' width='400' alt = 'prototype_ex3'/>
        <span>*추천 화면입니다*</span>
        <img src = '/img/now1.png' width='600' alt = 'prototype_ex3'/>
        <span>*현재 제작중인 페이지의 화면입니다. 추후 완성본은 다를 수 있습니다.*</span>
    </div>

## 배경
과거 20%의 주 품목들이 전체 매출의 80%를 차지하였다. 그러나 점차 개인 성향이 중시되며, 인터넷의 성장으로 정보의 접근이 쉬워지자 나머지 80%의 비주류 품목의 전체 매출이 무시 못할 규모가 되었다. 최근 IT 기업들은 이러한 현상 주목하고 개인 성향을 중시한 추천 알고리즘으로 시스템을 구축하기 시작하였고, 그 결과 매출 및 점유율 괄목할만한 결과를 얻어내었다. 추천 시스템의 등장은 시장의 패러다임과 라이프 스타일을 바꾸는 등 사회 전반에 영향을 미치고 있다. 이에 평소 알고리즘에 관심이 많았던 캡짱스톤조는 추천 알고리즘을 실제 적용하고 이해해보고자 추천 시스템을 구현하려고 한다.

- 목표 및 기대효과
    * 간편한 UI/UX 제공으로 쉬운 시간표 제작
    * 강의 몰림현상을 줄임
    * 좋은 강의들의 인원 부족으로 인한 강의의 폐강을 줄임
    * 학생들의 성향 파악을 통한 추천으로 만족도를 높이고 수강 포기 확률 감소
    * 정보의 불균형을 해소를 통한 수업 만족도 증가
- 관련 분야 survey
    * Stanford Jeffrey D. Ullman *mining massive datasets* 강의 수업자료
        * 기본적인 Recommend System 개념 학습
        * 신뢰도 계산법 및 적절한 선택법 학습
    * 카이스트 제 8회 ROSAEC 워크샵자료 *Recommendation System* "협업 필터링을 중심으로"
        * 기본적인 Recommendation System 개념 학습
    * mahout을 이용한 recommendation system Overview
        * recommendation system library 확인
    * `python` 과 `mysql` linking, 기존에 가지고 있던 데이터 마이닝 연습
        * `python`으로 `mysql`에 있는 데이터 변경 후 원래 서버와 linking하여 저장하는 연습이 필요

### 유사 프로젝트 검색 및 해당 프로젝트 결과물들의 문제점
-  [인하대학교 수강신청, http://sugang.inha.ac.kr/sugang/](http://sugang.inha.ac.kr/sugang/) : 학교 수강신청 사이트
    * 강의 선택이 한 화면에서 이뤄지지 않음
    * 모바일에 최적화 되어있지 않음<br/>
    <img src = '/img/com1.png' height="450"/>
    <img src = '/img/com2.png' height="350"/>
    * 컴퓨터 에서 본 화면입니다.<br/>
    <img src = '/img/phone1.png' height="400"/>
    <img src = '/img/phone2.png' height="400"/>
    * 모바일에서 본 화면입니다.<br/>


- [에브리타임, http://everytime.kr/](http://everytime.kr/) : 시간표 제작 및 익명 커뮤니티
    * 추천 시스템 부재
    * 실제 시간표가 수강신청 사이트에 등재 된 후 약 1주일 후 반영<br/>
    <img src = '/img/com3.png' height="300"/>
    <img src = '/img/com4.png' height="300"/>
    * 컴퓨터 에서 본 화면입니다.<br/>
    <img src = '/img/phone3.png' height="350"/>
    * 모바일에서 본 화면입니다.<br/>


- [SNUTT, http://snutt.kr/](http://snutt.kr/) : 서울대학교 시간표 제작
    * UI/UX 디자인 부재
    * 서울대 자대에만 사용되는 시스템
    * 추천 시스템 부재<br/>
    <img src = '/img/com5.png' height="400"/>
    * 컴퓨터에서 본 화면입니다.<br/>
    <img src = '/img/phone4.png' height="400"/><br/>
    * 모바일에서 본 화면입니다.


- [주관식 강의백서,https://goo.gl/PKoyQc](https://goo.gl/PKoyQc) : 인하대학교 주관식 강의백서
    * 불편한 UI/UX
    * 어려운 검색, 강의에 대한 자료의 낮은 가독성
    * 모바일 최적화 부재
    * 단순한 엑셀자료, 데이터 부족<br/>
    <img src = '/img/com6.png' height="350"/><br/>


- 기존 프로젝트와 제안 내용과의 차이 및 기존 문제 해결 방안
    * 추천 시스템
    * 사용이 간편한 UI/UX
    * 다양한 환경에서 사용가능 해야 한다.


- 기술적인 어려움
    * 특정 OS 기반이 아닌 브라우저 기반의 디바이스 최적화
    * 다양한 브러우저 호환 필요
    * 특정 기간에 급격히 늘어나는 요청에 대한 대응 필요
    * 잦은 연산에 의해 로드가 커져 시스템을 분리 필요
      * 단순하게 RDBMS를 폴링하는 방식은 급격히 늘어나는 요청에 제대로 대응이 힘듬
      * 시스템의 분리로 인한 시스템간의 효율적인 통신 방법의 필요성
    * 강의에 해당하는 데이터를 정보 통신처에서 직접 얻지 못해 크롤링을 하여 사용함
        * 크롤링이 적절하게 모두 이뤄지는지에 대해 검토 필요
        * 데이터가 모두 공통적인 속성을 갖고 있지않아 적절한 평가와 추천을 위해 데이터가공이 필요함
        * 크롤링 하는 데이터가 정규화되어 있지 않아서 사용하기 위해서는 한번더 가공이 필요함
    * 악의적 데이터 입력과 추천 몰림 현상으로 적절한 추천이 이뤄지지 않을 수도 있음
        * 이 악의적 데이터를 어떻게 관리할지에 대한 정책이 필요함
    * 새로 추가되는 강의를 추천할 때 어떠한 방식으로 할 지에 대한 방식또한 고민이 필요
        * 새로 추가되는 강의는 평가를 할 수 없음

## 개발 내용
* 개발 플랫폼 : **Web** <br/>
    1. 높은 호환성(OS에 국한되지 않음)<br/>
    2. 자바스크립트 기반의 높은 확장성<br/>
    3. 상대적으로 많은 라이브러리와 자료 존재<br/>
    4. 서버 언어로 `Node.js`를 사용하여 런닝 커브를 최소화<br/>

- 상세 요구사항
    * 기능적 요구사항 (functional requirements)
        * 과목 recommendation systems
        * 시간표 제작
        * 모바일 환경을 고려한 반응형 웹
        * 기존보다 쉽고 간편한 검색
    * 비기능적 요구사항 (non-functional requirements)
        * 해당 과목에 관심이 있는 인원 명시를 통한 경쟁 가능성 제시로 수강 인원 분산 유도
        * 추천 시스템 사용 유도
        * 플로우차트(다음페이지 상세)
    <div>
        <img src = '/img/flowchart.png' height="970"/>
        <span>*플로우차트입니다. 가로로 출력했습니다.*</span>
    </div>

## 개발 방법
- Web Application 개발을 위한 Open Source
  - React
      - facebook에서 만든 유저인터페이스 라이브러리
      - 페이스북, 인스타그램, 넷플릭스와 같은 웹 기반의 서비스에서 가장 널리 쓰고 있는 자바스크립트 프레임워크
      - 향후 모바일 앱을 만들때도 `React-native`를 사용해서 쉽게 포팅이 가능하다.
      - UI를 component를 통해서 UI의 재사용이 쉬워진다.
      - VIRTUAL DOM이라는 개념을 사용해서 상태의 변경에 반응하여 UI가 자동으로 변화되는 것이 특징
  - Babel
      - `ES6`와 `ES7` 모든 웹 브라우저에서 호환 가능하도록 변환해주는 transcompiler
  - Redux
      - 페이스북이 제시한 새로운 `Flux` 아키텍처의 구현체
      - `React`로 이루어진 앱에서 효율적인 데이터 흐름을 위해 사용하는 라이브러리
      - `Eco-system`이 성공적으로 유지되고 있어서 많은 사람들이 `Redux`기반의 라이브러리를 만들어내고 있다.
  - Node.js
      - `Javascript` 다양한 환경에서 사용할 수 있는 런타임 환경으로써, Non-blocking I/O와 단일 스레드 이벤트 루프를 통한 높은 처리 성능이 특징. 브라우저 기반의 자바스크립트를 확장
      - `Javascript` 기반이기 때문에, 상대적으로 프론트앤드와 같이 준비하기에는 런닝 커브가 낮다.
      - 내부 웹서버의 성능이 좋아서 상대적으로 배포가 쉽다.
  - express
      - `Node.js`에서 가장 많이 쓰이는 웹 프레임워크
  - passport
      - `Node.js`에서 가장 많이 쓰이는 유저 인증을 위한 미들웨어
  - SASS
      - `CSS`를 확장하는 pre-processor
  - webpack
      - `Javascript`와 각종 정적파일의 모듈화와 개발 서버를 제공해주는 라이브러리      
  - mysql
      - 가장 널리 쓰이고 있는 오픈소스 RDBMS
  - redis
      - 메모리 기반의 key/value NoSQL DBMS
  - lodash
      - 자바스크립트 기능 확장 라이브러리
  - beautifulsoup4
      - 파이썬기반의 html 파싱 라이브러리
- 추천 : **특정 교수님의 강의를 추천해줍니다.**
    * 사용하는 방식 : Collaborative filtering
        * 유사도 측정
            1. Cosine-similarity : 가장 많이 사용하는 방식. sparse한 데이터에 적합합니다.
            2. Manhattan Distance / Euclidean Distance : Missing value가 적을 때 효과를 발휘한다. dense한 데이터에 많이 사용합니다.
            3. Pearson Correlation Coefficient : grade-inflation 이 있는 곳에 적합합니다.
        * 저희의 점수 입력방식은 학생들이 모든 데이터를 입력할 것이란 보장이 없기에 sparse한 데이터 구조를 띄게 될 것입니다.
            * 그래서 시작을 Cosine-similarity로 하게 되었습니다.
            * 이후 MAE가 낮게 나와 신뢰도가 낮게 판단이 된다면 다른 방식을 찾아 반영할 예정입니다.
    * 실제 구현하는 방식
        1. 먼저 개인의 강의 성향을 파악하기 위해 수강했던 과목에 점수를 입력하게 됩니다.(1점 ~ 10점)
        2. 입력받은 점수를 기반으로 각 사용자들과 Similarity를 구하게 됩니다. 이 방식으로 Cosine-similarity를 사용합니다.
        3. 유사도를 구하여 가장 유사도가 높은 K명의 집단을 구합니다.
            * 여기서 저희는 계산횟수와 신뢰성을 높이기 위해 과 내에서 검색을 하게 됩니다.
        4. K명의 유사집단 내에서 제가 듣지 않은 과목을 찾고 그 과목에 해당하는 예상 평점을 유사도를 이용하여 계산합니다.
        5. 이후 이 예상 평점이 높은 과목을 추천하게 됩니다.
            * 만약 그 과목을 수강하고 이후에 그 과목에 대한 평점을 입력 했을 때 MAE를 계산하게 됩니다.
            * 주기적으로 유저의 MAE를 확인하여 제대로 추천이 되고 있는지 판단하여 알고리즘을 개선합니다.
- 가용 가능한 data sources
    - sugang.inha.ac.kr에서 수강가능한 시간표
    - 에전 총학생회에서 조사한 주관식 교양 백서
    - 인하대학교 정보통신처에서 학생들의 수강신청 기록들
        - 위 사항은 정보통신처에서 연락을 주지 않아 불가능할 것으로 예측됩니다.
    - '인하대학교 시간표'에서 데이터 요청
        - 위 데이터는 입력 받아 사용할 알고리즘(cosine-similarity)를 파이썬과 몽고디비를 이용하여 구현해보는데 사용했습니다.
        - 결과<br/>
            <img src = '/img/res1.png'/>
            * 위 과목을 들을 예정이던 학생과 비슷한 성향을 가진 학생을 찾아 유사도를 판단하고 그 유사도를 가진 학생들이 내가 선택하지 않은 어떤 과목을 선택했는지에 대해 검토해 보았습니다.
            <img src = '/img/res2.png' height='220'/>
            * 유사도 측정 후 가중치를 둬 과목에 합을 구한 결과입니다. 이 결과를 변환해 보면
            <img src = '/img/res3.png' height='100'/>
            * 이러한 과목을 다른 학생들은 선택했던것을 알 수 있습니다.
    - 크롤링한 데이터를 바로 사용할 수 있는 상태가 아니기 때문에 가공이 필요
        <img src = '/img/pro1.png' height='300'/>
        * 크롤링한 데이터의 시간 부분을 예로 들면 각 시간이 균일하게 나타나지 않는 것을 볼 수 있습니다.
        * 이것을 어떻게 균일하게 만들고 자동화 시킬지에대한 고민 또한 필요합니다.
- DB구성 예정(다음페이지 상세)
<img src = '/img/db.png' height='1000'/>
    * 추후에 다른 DB 테이블이 추가/삭제/변경 될 수 있습니다.
- 윤리, 정책 등 비기술적 고려사항
    - 평가가 이뤄지는 시기(6월)가 수강신청이 실제로 이뤄지지 않는 시기
    - 학생들의 지속적인 유입 방안 필요
    - 정보 수집 범위
        - 회원 가입시 정보 수집에 대한 동의
        - 개인정보 없이 직접적인 강의 평가를 받아 정보 누적
    - 학생들의 악의적으로 입력하는 데이터의 필터링 문제

### 계획 및 일정 (Plan and schedule)
- 프로젝트 규모 산정
    - 예상 소요기간
        - 기획 및 디자인 : 2017.03.02 ~ 2017.03.27
        - 개발 기간 : 2017.03.27 ~ 2017.05.31
        - 성과 측정 기간 : 2017.06.01 ~ 2017.06.15
    - 프로젝트 규모 : 두개의 서버(추천서버, 웹서버)와 8개(예정)의 뷰
- 요소 작업들에 대한 roadmap 구성
    * Gantt chart를 이용한 각 구성 작업 당 소요 기간(다음페이지 상세)
    <div>
      <img src = '/img/new_gantt.PNG' height='970' alt = 'gant_ex1'/>
      <span>*간트차트 입니다.*</span>
    </div>
- 평가기준
    - 알고리즘 개선에 따라 강의 추천의 정확도가 올라가는 것을 확인
        - MAE(Mean Absolute Error) : 예측 점수와 실제 점수의 차이를 측정하여 평균을 낸다. 이를 통해 해당 알고리즘의 정확성과 가중치를 판단 할 수 있습니다.<br/>
        <img src = '/img/mae.png'/><br/>
        - MAE값이 낮을 수록 점수 예측이 잘 된것이고 신뢰성있게 추천이 되었음을 의미합니다.
    - 추천 시스템 연산의 속도
        - 사용자의 요청에 따라 추천을 해줘야하는데 이때 많이 일어나게 되는 연산을 어떻게 나누게 될 지에 대해, 데이터 관리를 어떻게 할지에대해 평가가 이뤄져야 합니다.
    - 사용자의 웹/모바일 환경 접근성 향상 및 기존 사이트보다 편리한 UI/UX 제공 여부

#### 참고문헌
* Stanford Jeffrey D. Ullman *mining massive datasets* 강의 수업자료(http://infolab.stanford.edu/~ullman/mmds/ch9.pdf)
* 카이스트 제 8회 ROSAEC 워크샵자료 *Recommendation System* "협업 필터링을 중심으로"(http://rosaec.snu.ac.kr/meet/file/20120728b.pdf)
* 미네소타 대학 Technical Report, "Application of Dimensionality Reduction in Recommender System -- A Case Study"
* mahout을 이용한 recommendation system Overview(https://mahout.apache.org/users/recommender/recommender-documentation.html)
* mysql-python connector overview(https://dev.mysql.com/doc/connector-python/en/connector-python-connectargs.html)
* facebook official React document(https://facebook.github.io/react/)
* Redux offical document(http://redux.js.org/)
* Express official document(https://expressjs.com/en/api.html)
* Webpack2 offical document(https://webpack.js.org/)
* Mostly adequate guide to FP (in javascript)(https://www.gitbook.com/book/drboolean/mostly-adequate-guide/details)
* BeautifulSoup4 official document(https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
* Amazon Web Service official Document(https://aws.amazon.com/ko/documentation/)
* 인사이드 자바스크립트(http://www.hanbit.co.kr/store/books/look.php?p_code=B6479856408)
*
