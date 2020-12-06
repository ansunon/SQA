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