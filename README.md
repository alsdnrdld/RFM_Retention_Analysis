# RFM_Retention_Analysis

# 1. 프로젝트 개요

## 1 ]  분석 배경

**전자지급결제대행(PG**) 시장 점유율 싸움에서 **누적 사용자 281만명, 누적 거래액 8조원** 이라는 높은 성과를 달성하고 있으며 현재  **많은 기업과의 파트너십**(PayBack, 할인 제공)을 유지 중인 간편결제 서비스 *‘차이’ APP* 에 흥미를 가지게 되어 프로젝트 주제로 선택 하였습니다.

차이코퍼레이션에서 제공받은 실무 데이터와 관련 보도 자료를 살펴보던 중 다음과 같은 특징을 알게 되었습니다.

<br/>
<br/>

### ■ 온라인 쇼핑 시장에서 모바일 쇼핑 거래액 비중이 증가
<img src = "https://user-images.githubusercontent.com/85742844/166093727-0037d8b2-79d9-4868-8564-79573a3541a7.png" width="80%">

<br></br>
### 📈**간편 결제 서비스 현황**

- 구매의 편의성(결제, 정보 획득)의 증가와 코로나 19의 영향으로 온라인 구매를 선호
- 쇼핑 총 거래액은 1조 7,067억 원 (전년 동월 대비 11.5% 상승)
- 2013년 이래로 **쇼핑 총 거래액 중 모바일쇼핑 거래액 비중**이  **75.5 %로 역대 최대치를 달성**
- 간편 결제 서비스 하루 평균 이용 건 수 **1,821만건, 이용액 일평균 5,590억원** 으로 전기 대비   23.5% , 13.1% 증가

<img src="https://user-images.githubusercontent.com/85742844/166094621-a8557488-e9d2-45c2-9727-0a221dbad034.png" width="80%">

<br></br>

<aside>
📝  유통업계가 ‘간편 결제 시스템’ 전쟁을 벌이고 있다. 흔히 ‘○○페이’로 불리는 것들이다. 간편 결제는 모바일 기기에 신용카드나 계좌번호 등의 결제 정보를 등록해 비밀번호 입력, 지문인식만으로 결제할 수 있게 한 방식이다. 초기에는 이커머스 위주로 도입이 이뤄졌지만 최근에는 오프라인 기반 유통사도 적극적으로 뛰어들고 있다.  (2022-03-09. 쿠키뉴스,한전진 기자) <br>(http://www.kukinews.com/newsView/kuk202203080219](http://www.kukinews.com/newsView/kuk202203080219)</br>

</aside>

<p/>

<aside>
  📝 <b>전체 동향 최근 기사 </b>

이들이 간편 결제 시스템에 뛰어든 이유는 간단하다. 충성 고객을 확보하는 것은 물론, ‘데이터’를 확보하기 위함이다. 고객의 쇼핑 패턴을 빅데이터화 하여 ‘맞춤 마케팅’을 구현하겠다는 것. 이를 통해 고객들을 가둬두는 록인(Lock-in) 효과를 노린다는 복안이다. 현재는 고객 구매정보의 대부분이 카드사로 향한다는 점에서 한계가 있다.

</aside>

### ■ 많은 경쟁사가 존재하는 간편 결제 서비스 시장 
<img src="https://user-images.githubusercontent.com/85742844/166094913-aa52cf99-b6a0-420d-b0d9-369b16bf8117.png" width ="80%">

<img src="https://user-images.githubusercontent.com/85742844/166094916-5746faff-ada3-4ba7-91a8-1fbd06b267aa.png" width ="80%">

<br></br>

### ■ 프로젝트에서 무엇을 하고 싶은가?
사용량이 증가하는 만큼 경쟁사도 많은 간편 결제 시장에서 차이코퍼레이션이 생존하기 위해서는 차이코퍼레이션을 사용하는 고객들의 유지가 중요하다고 판단하였습니다. 

이번 프로젝트에서는 차이코퍼레이션의 많은 고객들 중 수익 기여도가 높은 사용자의 특징을 알아내고 수익 기여도가 높은 고객들을 대상으로 어떤 전략을 세워야 하는지를 데이터 분석을 통해 알아보고자 하였습니다. 

<aside>
  <ul>
  <li>상위 고객 그룹을 세분화하기 위해 RFM 분석을 진행. </li>
  <li>코호트 분석을 이용한 고객 이탈률 파악</li>
  <li>파레토 분석을 활용하여 매출 기여도가 높은 고객층 파악 후 분석 대상 설정</li>
  <li>마케팅 대상과 시점의 선별을 위해 상위 고객 군의 연령, 성별 , 사용 시간 등을 분석.</li>
  </ul>
</aside>

<img src="https://user-images.githubusercontent.com/85742844/166094912-d16c6e17-23a6-4fae-85fa-01e3540d364f.png" width ="80%">
<br></br>

## 2 ] 개발 환경
<img src="https://user-images.githubusercontent.com/85742844/166094917-28fff305-f611-4fc8-be86-13f32138d5a8.png" width ="80%">
<br></br>

### 1. Google Drive

- Google Drive에 공유 폴더를 생성
- 모든 팀원들과 작업내용 공유 및 피드백
- 데이터 백업 및 데이터 통합 관리

### 2. Python

- 데이터 전처리, 시각화
- 파레토, 코호트, RFM 분석기법 사용
- Clustering 기법을 활용하여 분석 대상 선정 및 목표 설정

### 3. Google Colab

- 코랩 주피터 노트북을 사용해 실시간으로 팀원들과 작업 내용을 공유
- 구글 드라이브의 공유 폴더와 연결하여 분석 실행

### 4. Tableau

- 대시보드를 활용한 종합적인 시각화 수행
- Tableau Public과 Google Drive 공유 폴더를 활용하여 작업내용 공유 및 관리

<br></br>
<br></br>
# 3. 데이터 소개 및 전처리


## 1 ] 어떤 데이터를 사용하였나? 

       → 차이코퍼레이션의 2019-08-01부터 2020-03-31 까지의 데이터를 사용

## 📎기존 데이터
![image](https://user-images.githubusercontent.com/85742844/166098239-f29e352a-0d09-4d4a-aaaf-fc22ff1dd329.png)



## ⚙️Feature Engineering
![image](https://user-images.githubusercontent.com/85742844/166098250-655c7646-12de-485a-a075-6707d2858a1b.png)


## 🥇고객 등급 기준

: Feature Engineering을 통해 만들어진 칼럼들을 활용하여 고객 등급 기준과 코드에 대한 정보를 담고 있는 데이터 셋 생성
![image](https://user-images.githubusercontent.com/85742844/166098259-3f25b9f0-a4b3-44a1-8b97-1b27a812399f.png)


## 2 ] 어떤 분석 방법을 사용 하였나?

### 1 )  RFM 분석

고객을 R,F,M 세가지 기준에 따라 수익에 기여를 많이 하는 고객을 선별하는 기법

![title](https://user-images.githubusercontent.com/85742844/166098282-ff3cf28b-0bb1-40f6-a846-8b9d538e5f3f.png)
<br/>

거래의 최근성, 거래의 빈도수, 거래의 규모를 기준으로 고객들에게 코드를 부여하고 부여된 코드들을 공통점으로 묶어서 등급을 매기는 분석 방법

<br/>

![image](https://user-images.githubusercontent.com/85742844/166099005-929defc8-c46a-46b8-b34b-5112e7ced754.png)


<br/>

### 2 ) 파레토 차트

파레토 원칙이 성립하는지를 차트를 통해 확인 해보고 파레토 원칙에 입각하여 수 많은 고객군들 중 분석할 고객군을 선정.

<br/>

![image](https://user-images.githubusercontent.com/85742844/166351119-ffbaaa4c-26bf-48d5-a48e-d1bab218c94a.png)

<br/>

### 3 ) 코호트 분석

고객군의 공통된 행동 및 경험을 분석하여 소비 트랜드를 알아내고 그에 알맞는 전략을 제시하고자 함

<br/>

![image](https://user-images.githubusercontent.com/85742844/166353224-aab9301e-ca62-4bee-9be0-d205da287e20.png)

<br/>

<br/>

<br/>

## 3 ] 데이터 전처리 : EDA

### 1 ) 결측치 확인

### ▶ **Missingno 사용하여 결측치 확인**

![image](https://user-images.githubusercontent.com/85742844/166355891-95c907e7-acfc-4a3d-a841-6b910437ff46.png)




