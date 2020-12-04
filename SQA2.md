# Software 개발 모델
### 폭포수 모델(waterfall) 
> "순차적으로 진행"

![폭포수모델](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e2/Waterfall_model.svg/350px-Waterfall_model.svg.png)

### 반복/점증적(iterative/incremental) 개발 모델
ex) 애자일

![반복/점증적 모델](https://upload.wikimedia.org/wikipedia/commons/thumb/3/39/Iterative_development_model.svg/440px-Iterative_development_model.svg.png)


### V - model (폭포수 모델에서 나왔다.)
![v - model](https://www.researchgate.net/profile/Dirk_Sauer/publication/322477987/figure/fig11/AS:668599689687056@1536417996787/V-model-of-SW-development-process-inspired-by-1-3.png)

|종류|Verification|Validation|
|-|-|-|
|정의|개발단계의 산출물의 그 단계의 초기에 설정된 요구 조건을 만족하는지 여부를 결정하기 위해 구성 요소나 시스템을 평가하는 프로세스|명시된 요구사항을 만족하는지 여부를 확인하기 위해 개발단계 말/중간 에 구성요소나 시스템을 평가하는 프로세스|
|특징|인간에 의해 테스팅 <br/>(=주로 산출물 위주의 검토)|컴퓨터기반 테스팅 <br/>(=실제로 소프트웨어를 수행)|
|종류|인스펙션, 워크쓰루, 동료 검토 등<br/><br/> - 주기 검증: 개발 주기의 특정단계에서 제작된 제품이 이전단계에서 설정한 기준을 만족하는지 결정<br/> - 형식 검증: 원시 부호가 규격에 맞게 작성 되었는지를 수학적으로 증명|- 하위 레벨 테스팅<br/>(단위, 통합 테스팅) / <br/><br/>- 상위 레벨  테스팅<br/>(사용성/ 기능/ 시스템/ 인수 테스팅)|
|종류|인스펙션, 워크쓰루, 동료 검토 등|- 하위 레벨 테스팅<br/>(단위, 통합 테스팅) / <br/><br/>- 상위 레벨  테스팅<br/>(사용성/ 기능/ 시스템/ 인수 테스팅)|

### 개발환경과 테스팅
- 모든 개발활동은 테스팅 활동과 대응한다.<br/>
= 테스트 활동은 개발이 완성된 다음에 시작되는 것이 아니다.
- 각 테스트 레벨은 각 개발단계로 테스트 대상(범위) 및 목적에 따라 분류된다.  
- 각 테스트 레벨 별 테스트 준비활동(분석/설계/구현 등)은 개발 수명 주기 동안 진행된다.<br/>
= 테스트계획, 테스트 케이스 개발, 테스트 환경 준비 등
- 테스터는 개발 수명주기 동안에 개발 산출물 생성시 해당 문서에 대한 리뷰 활동에 참여한다.
- 테스트 수행 산출물에 대한 검토(리뷰 등) 활동 필요하다.<br/>
= 테스트 계획, 테스트케이스, 테스트 환경, 테스트 결과 결함 보고서 등