### 구조 기반 테스트 
    - 소프트웨어/시스템 구조(Structure)를 중심으로 테스팅 
    - Software 경로(path), 구조(Structure)와 구현(Implementation)에 기반한 테스트 설계 기법
    - 일반적으로 프로그래밍 스킬 필요

- 구조 기반 테스팅 수행 절차
    1. 구현된 소프트웨어 분석
    2. 소프트웨어의 실행 경로(if, while, for, switch ...) 식별
    3. 선택된 경로가 실행되는 입력 선택
    4. 각 입력에 대해 기대되는 출력을 결정
    5. 테스트 수행
    6. 기대 결과 와 실제 결과 비교

- 테스트 커버리지 개념
    - 테스트의 충분성을 측정하기 위한 정량적 지표
    - 시스템/소프트웨어의 구조가 테스트 스위트에 의해 테스트된 정도
        - 전체 소스코드에서 실행된 코드의 비율은 몇 %인가?
        - 실행 안된 코드에 결함은 없는가?

### 제어 흐름 테스팅
    - 프로그램 코드상 수행 경로(excution path)를 정의하고, 그 경로를 수행하는 테스트
    - 프로그램 내의 모든 독립적인 경로 수행 → 프로그램 내에 존재하는 모든 경로 탐색
    - 일반적으로는 사용되지 않는 조합에서 발생할 수 있는 오류들 검출 가능

- Decision(결정)은 하나 이상의 Condition(조건)으로 구성
    ```(java) 
    if(x>0 && y==0)
    ```
    - if(): Decision(결정) or Branch(분기)
    - x>0, y==0: Condition(조건) 

![](https://lh3.googleusercontent.com/proxy/A3VjN7Tdu_vCgDfigbKXB19LPWS58PiFvbT49sAXq1iTss8Df1C0cU7p84mQ91VKDpICxMYZ-NauNPfoKLs83v4Z_-aO9EN45eHxDX81zXOFH7g7-gmD8-Dx)

#### 구문 커버리지(Statement Coverage)
> 100% 구문 커버리지는 테스트 중에 프로그램 내의 모든 문장이 적어도 한번 실행된다는 의미
    - 100% 구문 커버리지 달성 용이 → 낮은 강도의 커버리지 수준
    - 실무적으로 100% 달성이 불가능한 경우가 많음 → 예외 상황 수행을 위한 소스코드 구현이 어려울 경우 발생


#### 결정 커버리지(Decision Coverage/ Branch Coverage)
    - 100% 결정 커버리지는 테스트 중에 프로그램 내의 모든 결정 분기가 적어도 한번씩은 실행됨
    - 100% 결정 커버리지는 100% 구문 커버리지를 보장한다.

#### 조건 커버리지(Condition Coverage)
> 100 조건 커버리지는 테스트 중에 프로그램 내의 각 결정을 구성하는 조건의 결과가 적어도 한번씩은 나타남을 의미</br> (100% 조건 커버리지가 100% 결정 커버리지를 만족하는 것은 아니다.)

#### 조건/결정 커버리지(Condition/Decision Coverage)
> 100% 조건/결정 커버리지는 테스트 중에 프로그램 내의 각 결정이 최소 한번씩 수행되며, 이를 구성하는 조건의 결과가 적어도 한번씩은 나타남을 의미

#### 변형 조건/결정 커버리지(Modified Condition/Decision Coverage)
> 각 개별조건식이 다른 개별 조건식에 무관하게 전체 조건식을 결과에 독립적으로 영향을 주도록 함으로써 조건/결정 커버리지를 개선한 방식


#### 다중 조건 커버리지(Multiple Condition Coverage)
    - 100% 다중 조건 커버리지는 테스트중에 프로그램  내의 모든 Decision 내의 모든 Condition의 결과에 대한 모든 조합을 고려한다.
    - 개별 조건식의 가능한 조합 고려한 강력한 논리적 수준의 커버리지