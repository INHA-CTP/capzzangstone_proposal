<center><h1>종합설계 제안서 (구성중)</h1></center>
<div style = "text-align:right; font-size: 17px;">한정(컴공, 12114497), 박인규(컴공, 12121484), 이강호(컴공, 12142380)</div>
---

## 주제

<h5>최종목표 : **한마디로 정리할 수 있는 우리의 목표**</h5>
* 시간표를 웹, 모바일 웹 모두에서 쉽게 작성할 수 있게 도와준다.<br/>
* 현재의 성향을 파악하여 과목을 추천 받을 수 있게된다.<br/>
* 강좌의 선택 폭이 다양해질 수 있다.<br/>
* 몇명이 이 과목에 관심이 있는지 알 수 있다.<br/>

- UI prototype
    <div style = 'margin:10px;'>
        <img src = '/img/1.png' width='400' alt = 'prototype_ex1'/><br/>
        <span>*메인 화면입니다.*</span>
    </div>
    <div style = 'margin:10px;'>
        <img src = '/img/1.png' width='400' alt = 'prototype_ex2'/><br/>
        <span>*프로토타입2*</span>
    </div>
    <div style = 'margin:10px;'>
        <img src = '/img/1.png' width='400' alt = 'prototype_ex3'/><br/>
        <span>*프로토타입3*</span>
    </div>

## 배경
현재 외국 IT기업들은 과거 *파레토 법칙* 과 반대되는 *롱테일 현상* 에 기반하여 개개인에 맞춤 추천을 한다.<br/>
이에 관심이 많았던 조원들은 실제로 학교 내에서 학생들이 쉽게 사용할 뿐더러 추천 알고리즘을 테스트 할 수 있는 주제를 찾게 된다.<br/>
현재 외국 IT기업들은 과거 파레토 법칙 과 반대되는 롱테일 현상 에 기반하여 개개인에 맞춤 추천을 한다.<br/>
이에 관심이 많았던 조원들은 실제로 학교 내에서 학생들이 쉽게 사용할 뿐더러 추천 알고리즘을 테스트 할 수 있는 주제를 찾게 된다.<br/>

친분이 있는 이들의 추천만 듣게 된다 => 친분이 있다 하더라도 성향이 비슷하지는 않음<br/>
결국 획일화 된 강의 선택 => 수강생 쏠림 현상 => 비인기 강의 폐강<br/>

현재 상황은 결국 파레토 법칙처럼 베스트셀러들이 점거하고 있는 상황임<br/>
롱테일 현상에 기반한 강의 선택이 이루어지면 => 강의의 선택 폭이 넓어지고, 쏠림 현상도 개선(수강신청 때마다 전쟁이야!)<br/>
> 인규야 위에 내용 말좀 잘 털어줄 수 있음? => 지금 입 털기 장전 
- 이 프로젝트 완료로부터 기대되는 효과  
    * 간편한 UI / UX 제공으로 쉬운 시간표 제작
    * 강의 몰림현상을 줄임
    * 좋은 강의들의 인원 부족으로 인한 강의가 폐쇄됨을 줄임
    * 학생들의 성향 파악을 통한 추천으로 만족도를 높이고 강의를 포기할 확률을 줄임
- 관련 분야 survey
    * Stanford Jeffrey D. Ullman *mining massive datasets* 강의 수업자료
        * 기본적인 Recommend System 개념 학습
        * 신뢰도 계산법 및 적절한 선택법 학습
    * 또 다른 서베이가 들어가야 함
        * 그 어떤 무언가
- 유사 프로젝트 검색 및 해당 프로젝트 결과물들의 문제점
    * [인하대학교 수강신청, http://sugang.inha.ac.kr/sugang/](http://sugang.inha.ac.kr/sugang/) : 학교 수강신청 사이트
        * 강의 선택이 한 화면에서 이뤄지지 않아 매우 불편함
        * 모바일에 최적화 되어있지 않음
    * [에브리타임, http://everytime.kr/](http://everytime.kr/) : 시간표 제작 및 익명 커뮤니티
        * 추천 시스템 부재
        * 실제 시간표가 수강신청 사이트에 등재 된 후 1주일 정도 있다가 반영됨, 반영이 늦은편
    * [SNUTT, http://snutt.kr/](http://snutt.kr/) : 서울대학교 시간표 제작
        * UI / UX 디자인 부재
        * 서울대 자대에만 사용되는 시스템
        * 추천 시스템 부재
    * [주관식 강의백서](http://www.inha.ac.kr/user/boardList.do?command=view&page=1&boardId=235757&boardSeq=5371322&id=plaza_010100000000) : 인하대학교 주관식 강의백서
        * 불편한 UI / U.
        * 검색이 힘들고, 강의에 대한 자료들이 한눈에 들어오지 않는다.
        * 모바일에서 최적화가 이루어지지 않았다
    * [인하대 수강신청](sugang.inha.ac.kr) : 인하대학교 수강신청 사이트
        * 불편한 UI / UX
        * 모바일 최적화가 이루어지지 않았다
- 기존 프로젝트와 제안 내용과의 차이 및 기존 문제 해결 방안
    * 추천 시스템
    * 사용이 간편한 UI / UX
    * 그리고 등등등
- 기술적으로 어려움
    * 추천해주는 과목(item)이 적절하게 추천이 되었는지 추천을 받는 user의 만족도를 수량적으로 판단하기가 힘들다
        * 이 부분에 대해서는 자체 추천 알고리즘 소개 논문에서 성과 부분을 보면 도움이 될 것이라 예상
        * 아 그냥어려운데 2
    * 특정 OS 기반이 아니라 브라우저 기반이기 때문에 디바이스 최적화 문제가 어려움
    * 모든 학생이 사용해야 하기 때문에 모든 브라우저에 대응해서 만들어야 한다
    * 특정 기간에 급격히 늘어나는 요청에 대응할 수 있어야 한다
    * 비용이 큰 연산이 자주 일어나기 때문에, 시스템을 분리해야 한다.

## 개발 내용
* 개발 플랫폼 : **Web Application** <br/>
    1. 호환성이 좋다.(OS에 국한되지 않음)<br/>
    2. 자바스크립트 기반으로 만들어지기 때문에 차후에 스마트폰 어플리케이션이나 데스크탑 어플리케이션으로 만들기 수월하다.<br/>
    3. 상대적으로 많은 라이브러리들과 자료들이 있다.<br/>
    4. 서버 언어로 `Node.js`를 사용하기 때문에 클라이언트와 번갈아 가면서 개발하기 수월함.<br/>
- 상세 요구사항
   * 기능적 요구사항 (functional requirements)
        * 과목 recommendation systems
        * 시간표 제작
            * 모바일 웹으로도 검색이 쉽게 반응형 웹으로 제작되어야함
            * 검색부분이 기존
   * 비기능적 요구사항 (non-functional requirements)
     * performance (response time, throughput per unit time)
     * usability, reliability, security, safety, restriction, etc.
- 상세 구조 (system components and relation between components)
   * data flow diagrams, UML diagrams, flowcharts 등 도표를 활용할 것
<div style = 'margin:10px;'>
   <img src = '/img/flow_ex1.png' width='700' alt = 'flow_ex1'/><br/>
   <span>*플로우 차트입니다. 에제 입니다*</span>
</div>

## 개발 방법
1. 사용하게 될 open sources
  - React
    - facebook에서 만든 유저인터페이스 라이브러리.
    - 페이스북, 인스타그램, 넥플릭스에서 널리 쓰이고 있다.
    - UI를 component화 해서 재사용이 쉽게 만드는게 특징
    - VIRTUAL DOM이라는 개념을 사용해서 상태의 변함에 따라서 선택적으로 UI를 렌더링한다.
  - Babel
    - ES6와 ES7 모든 웹 브라우저에서 호환 가능하도록 변환해주는 transpiler.
  - Redux
    - React로 이루어진 앱에서 효율적인 데이터 흐름을 위해 사용하는 라이브러리
  - Node.js
    - Javascript 엔진으로 만들어진 언어로써, Non-blocking I/O와 단일 스레드 이벤트 루프를 통한 높은 처리 성능이 특징인 언어
  - express
    - Node.js에서 가장 많이 쓰이는 웹 프레임워크
  - passport
    - Node.js에서 가장 많이 쓰이는 인증을 위한 미들웨어
  - SASS
    - CSS를 확장하는 pre-processor
  - webpack
    - 자바스크립트 모듈화를 지원해주는 모듈화 엔진
  - mysql
    - 가장 널리 쓰이고 있는 오픈소스 RDBMS
  - redis
    - 메모리 기반의 key/value NoSQL DBMS
- 가용 가능한 data sources
  - sugang.inha.ac.kr에서 수강가능한 시간표
  - 에전 총학생회에서 조사한 주관식 교양 백서
  - 인하대학교 정보통신처에서 학생들의 수강신청 기록들
  - 예전에 잠깐 운영되었던 인하대학교 시간표라는 사이트에서 데이터 요청

- 윤리, 정책 등 비기술적 고려사항
    - 평가가 이뤄지는 시기(6월)가 수강신청이 실제로 이뤄지지 않는 시기
        * 이전 학기까지 들었던 과목 입력 후 현재 듣는 과목의 만족도를 비교 해보는 방식으로 평가 가능
    - 정보를 어디까지 수집해야 하는 문제
        - 개인 정보 동의란에 동의를 얻어 수집할 수 있음
        - 개인정보를 이용하지 않고 직접적인 평가를 얻어 추천을 하는 방식을 사용할 수도 있음
    - 학생들의 악의적으로 입력하는 데이터의 필터링 문제


### 계획 및 일정 (Plan and schedule)
- 프로젝트 규모 산정
    - 예상 소요기간
        - 기획 및 디자인 :
        - 개발기간 :
        - 평가기간 : 이걸 이용해서 간트차트 기간을 만들면 될 듯
    - 프로젝트 규모 : 이건 뭐 우리맘대로적는거에요?
- 요소 작업들에 대한 roadmap 구성
  구성 작업(task) 식별 및 PERT chart를 이용한 관계 명시: 독립적 작업 규명, 작업간 순서 결정
  마일스톤(중간 점검 단계에서 완성되어야 하는 기대 결과물) 명시
  시간, 인력 등 자원 할당
  Gantt chart를 이용하여 각 구성 작업 당 소요 기간 명시
   . 계획은 격주별로 할당되어야 함 (발표 대상 주를 고려하여 작성)
   . 각 작업에 대해 팀원 중 누가 책임을 질 것인지 명시
   . 2주 별, 각 팀원별 평가 기준 명시
   . 마일스톤(즉, 주요 중간 목표들) 명시
<div style = 'margin:10px;'>
  <img src = '/img/gant_ex1.png' width='700' alt = 'gant_ex1'/><br/>
  <span>*간트차트 예제입니다.*</span>
</div>
- 최종 결과물 평가를 위한 평가 기준
  . 정량적 목표: 달성하고자 하는 목표를 수치로 표시할 것
    (예) 검색 엔진 개발이라면, xx GB ram, xx TB disk, xx CPU 및 xx OS version xx가 탑재된 컴퓨터에 yy개 이상의 crawed page data를 저장한 상태로, 초당 xx 개 이상의 query를 처리
  . 정성적 목표: 수치화할 수 없는 목표를 기술할 것

#### 참고문헌
* web part
    * 이런 논문 1
    * 이런 사이트 1
    * 이런 논문 2
    * 등등등
* recommendation part
    * Stanford Jeffrey D. Ullman *mining massive datasets* 강의 수업자료(http://infolab.stanford.edu/~ullman/mmds/ch9.pdf)
    * 이런 사이트 1
    * 이런 논문 2
    * 등등등
