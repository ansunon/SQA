### 테스트 유형
![테스트 유형](https://www.tutorialride.com/images/software-testing/test-types.jpg)
___
</br>

#### ISO 25010 품질 특성
ISO(국제 표준화 기구)에서 제겅한 Software 품질 평가를 위한 Software 품질 평가 통합 모델 표준

![ISO 25010](https://lh3.googleusercontent.com/proxy/c6J_-bWNsmFRR7FGX9F7skRDwUkuJd5NwCz82qUPdNPiRRcgO3vFZtXYWrVctjSoaMl_ViA7hbVHzoUXvdkt9ttC3qS5MoKiyakWthAgyKQ)

#### 기능 테스트(Functional Testing)
- 개념: 컴포넌트나 시스템의 기능 명세에 정의된대로 작동하는지를 확인하는 테스팅 활동
- 명세 기반 테스트(Specification based Test) 수행
    - 컴포넌트나 시스템의 내부 구조를 참조하지 않고 기능 명세를 기반으로 Test Case 도출
    - 활용 가능한 Software 모델(요구사항 명세서, 기능 명세 등에 포함)
        1. 프로세스 흐름 모델(Process flow model)
        2. 상태 전이 모델(State transition model)
        3. 유즈케이스 모델(Use case model)
        4. 평문 언어 명세(Plain language specification)
- 특징
    - 모든 테스트 레벨(Test Level) 에서 수행</br>
    (컴포넌트에 대한 기능 테스트는 컴포넌트 명세 기반)

#### ISO 25010 에서 정의한 기능성 외 비기능성 특성에 기반한 Software Testing 유형

|유형|특징|
|-|-|
|기능 테스트|기능 요구 사항 검증|
|사용성 테스트</br>(Usability Test)|소프트웨어를 쉽게 사용할 수 있는 정도를 측정하고 검증 확인 하는 테스트|
|성능 테스트|시스템에 부하를 주면서 응답시간, 처리량, 속도 등 성능 지표 추이 측정|
|스트레스 테스트|복합 데이터 또는 대량의 데이터를 이용한 과부하 장기(Long-term) 테스트|
|회복 테스트|문제가 발생 했을 때 복귀 능력 검증 예) 장비 복구 테스트|
|보안 테스트|외부의 침입이나 해킹에 대응하는 능력 검증|

#### 비기능 테스팅(Non - functional Testing)
- 개념: 컴포넌트나 시스템의 기능성(Functionality)외에  비 기능적(Non-functionality) 품질 특성을 준수하는지 확인하는 테스트 활동)
    - 성능,부하, 스트레스, 사용성, 유지보수성, 이동성 등</br>
- 명세 기반 테스트(Specification based Test) 수행
    - 컴포넌트나 시스템의 내부구조를 참조하지 않고 명세 분석을 통해 비기능 테스팅을 위한 Test Case 도출
    - 국제 표준(ISO/IEC 9126 소프트웨어 제품 품질 모델 등) 또는 사내 품질 표준 기반으로 Test Case 도출
</br>
- 특징
    - 모든 테스트 레벨에서 수행(컴포넌트에 대한 기능 테스트는 컴포넌트 명세 기반)


#### 구조적 테스팅(Structural Testing)
- 개념: 컴포넌트나 시스템의 특정 유형의 구조 커버리지를 평가하여 테스팅의 보장성/충분성(Troroughness)을 추정하는 테스트 활동
    - 커버리지: 시스템 또는 소프트웨어의 구조가 테스트된 정도를 정량적으로 기술</br>

- 구조 기반 테스트(Structure based Test) 수행
    - 컴포넌트나 시스템의 내부 구조를 분석하여 Test Case 도출
        - 제어 흐름 모델 (Control flow model)
        - 메뉴 구조 모델 (Menu Structure model, Window navigation flow)</br>

- 특징
    - 모든 테스트 레벨에서 수행
        - 통합 테스트: Call Tree 구조 등
        - 시스템 테스트: 시스템 아키텍처, MBD 모델 구조 등

#### 확인/리그레션 테스팅(Confirmation and Regression Testing)
- 확인 테스팅(Confirmation Testing): 발견된 결함이 수정되어 제거 되었는지 확인하기 위한 테스팅 활동
- 리그레션 테스팅(Regression Testing): 수정에 따른 신규 결함이 유입 되었는지 확인하기 위한 테스팅 활동</br>

- 특징
    - Debugging 은 결함을 해결하는 활동으로 Testing 활동이 아니다.
    - 기존 Test Case 반복 수행하므로 자동화 대상이 된다.

