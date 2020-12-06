#### 결정 테이블 테스팅 기법(Decision Table Testing)
- 개념: 시스템 요구사항/ 비지니스 로직 등에서 원인과 결과를 분석하여 Test Case를 조합해 내는 방법</br>(Cause - Effect Diagram/Graphing)</br>

- 장점
    - 논리적으로 의존적인 가능한 모든 조건들의 조합을 생성 ▶ "촘촘"하게 테스트 가능
    - 요구사항 등 테스트 베이시스의 문제점을 드러내게 하는 효과적인 Test Case 생성 가능</br>
        ▶ Test Case 작성 중 리뷰 활동을 수행/ 테스트 베이시스의 불완전성과 모호함 지적 가능</br>

- 단점
    - 작성에 많은 노력과 시간이 소요될 수 있음(결정 테이블 작성후 개발팀 검토 필요시)
    - 복잡한 시스템을 표현하기 어려울 수 있으며, 논리적으로 작성시 실수의 소지 존재

- 결정 테이블 테스팅 작성법
    - Cause(원인)는 Input
    - Effect(효과, 결과)는 intermmediate results, message, outputs 등
    - Cause 와 Effect는 Boolean 형태로 기술</br>

- 결정 테이블 테스팅 예제
    - Specification
        - 사람들에게 50만원을 배당한다.
        - 만약 직업이 있고 연령이 40세 이상이면 10만원 더 준다.
        - 직업이 없는 사람의 경우 3자녀 이상을 두었다면 5만원을 더 준다.

    - Test Case Design
        - Cause
            - Cause 1: 직업이 있는지 없는지(T,F)
            - Cause 2: 연령이 40세 이상,미만(T,F)
            - Cause 3: 3자녀 이상을 두었는지 아닌지(T,F)</br>

        - Effect
            - Effect 1: 50만원을 받는다.
            - Effect 1: 10만원을 더 받는다.
            - Effect 1: 5만원을 더 받는다.</br>

    - Test Case 결과

|Cause|TC1|TC2|TC3|TC4|TC5|TC6|TC7|TC8|
|-|-|-|-|-|-|-|-|-|
|Cause 1|T|T|T|T|F|F|F|F|
|Cause 2|T|T|F|F|T|T|F|F|
|Cause 3|T|F|T|F|T|F|T|F|
|Effect|-|-|-|-|-|-|-|-|
|Effect 1|V|V|V|V|V|V|V|V|
|Effect 2|V|V|-|-|-|-|-|-|
|Effect 3|-|-|-|-|V|-|V|-|
|기대결과|60만원|60만원|50만원|50만원|55만원|50만원|55만원|50만원|


#### 상태 전이 테스팅 기법(State Transition Testing)
> 시스템을 상태 전이 다이어그램으로 표현하여, 이를 바탕으로 TC를 도출하는 기법</br>
- 특징
    - 이벤트, 액션, 활동, 상태, 상태전이 사이의 관계를 검증하는 테스트 기법(모든 상태/이벤트 조합을 확인)
    - 시스템/Software의 상태기반 행위가 명세된 내용과 일치함을 검증
    - 상태기반 시스템의 결함은 상태,상태 전이, 가드, 이벤트 결함 등으로 분류
    - 결함은 "구현이 잘못된 경우"와 명세가 잘못된 경우에 존재

    |구성|설명|표기법|
    |-|-|-|
    |State(상태)|하나 또는 그 이상의 이벤트를 기다리는 시스템의 모든 상태|원/표기와 같이 표기|
    |Transition(전이)|이벤트에 의해 한가지 상태에서 다른 상태로의 변경|화살표의 형태로 링크시켜 상태와 상태를 연결|
    |Event(이벤트)|상태의 전이를 유발하는 행위(요인)|화살표 위에 이름과 값으로 표기|
    |Guard(가드)|이벤트가 발생하는 조건|이벤트의 오른쪽 []안에 조건이나 값으로 표기|
    |Action(액션)|상태의 전이에 따라서 유발되는 동작|화살표에 이름과 값으로 표기|

    ![상태 전이 다이어그램](https://lh3.googleusercontent.com/proxy/bpTb9yAv1A-uIwvFe02Q4VBvab0H26LTCUgf22AtzlVnJCB2C2SUGvqpwgY0k4p6Zx5qj3w5FHCNF_WMuIsJ9PyduTN0oF5sRlj1J-JJWqu1Zq1YIAiHDOZw)

    ![상태 전이 테이블](https://image.slidesharecdn.com/istqb-4-2015-2-1-150512073105-lva1-app6892/95/istqb-4201521-10-638.jpg?cb=1431415911)

- Switch Level(테스팅 Depth)
    - 연속된 Transition들의 가운데 끼어 있는 상태를 Switch라고 함
    - Switch Level은 이러한 중간의 거치는 상태의 개수를 말함</br>


