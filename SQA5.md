### 테스트 개발 프로세스
#### 테스트 설게란?
    - 테스트 분석을 통해 Test Case를 도출하기 위한 전략 수집 활동
    - 테스트 대상 소프트웨어 제품 분석을 통해 테스트 전략을 구체화(접근 방법, 수준, 기법 등)
        - 순서: 테스트 베이시스 분석 ▶ 테스트 조건 식별/ 테스트 데이터 분석 ▶ Test Case 도출

#### 테스트 설계의 필요성
    - 모든 경우의 수를 테스트하는 것은 불가능하기 때문
    - 충분한 테스트 커버리지를 만족하면서 테스트 개수를 줄일 필요
    - 결함을 찾을 가능성이 높은 테스트 케이스를 식별 하기 위한 기법 필요
        - 테스트 설계시 결함 발생 가능성이 높은 곳을고려해야 한다.

#### Test Design and Implementation Process(ISO 29119)
- 주요 산출물
    - Test Design Specification
    - Test Case Specification
    - Test Procedure Specification</br>

- 테스트 케이스: 테스트 수행을 위한 최소 단위로서, 테스트 수행에 관한 내용을 기술

<table>
  <tr>
    <td rowspan="8">테스트 케이스 구성 요소</td>
    <td>종류</td>
    <td>내용</td>
  </tr>
  <tr>
    <td>ID</td>
    <td>Test Case 식별 번호</td>
  </tr>
  <tr>
    <td>사전 조건</td>
    <td>테스트 수행전 선결되어야하는 조건에 대한 정보(구동 환경, 데이터 초기화 등)</td>
  </tr>
  <tr>
    <td>수행 순서</td>
    <td>구체적인 테스트 수행 절차</td>
  </tr>
  <tr>
    <td>기대 효과</td>
    <td>테스트 수행 후 의도한 대로 동작하였는지 판단 근거, 필요시 사후 조건(Post-condition) 기술</td>
  </tr>
  <tr>
    <td>추적성</td>
    <td>해당 테스트와 연관된 산출물 항목 기술</td>
  </tr>
  <tr>
    <td>중요도</td>
    <td>시간적 제약 발생시 선택 기준</td>
  </tr>
  <tr>
    <td>합격/불합격</td>
    <td>테스트 수행 결과 판정(Pass/Fail/Not Tested/Blocked)</td>
  </tr>
</table>

#### 테스트 설계 기법의 구분 
> 테스트 대상을 인삭하는 방법에 따라 달라진다

<table>
    <tr>
        <td>종류</td>
        <td>특징</td>
    </tr>
    <tr>
        <td rowspan="3">블랙 박스 테스트</td>
        <td>시스템 내부 구조를 고려하지 않음</td>
    </tr>
    <tr>
        <td>Test basis/개발자 및 테스터 경험 분석</td>
    </tr>
    <tr>
        <td>주로 Software의 행동(behavior)에 대해 노력 집중</td>
    </tr>
    <tr>
        <td rowspan="3">화이트 박스 테스트</td>
        <td>컴포넌트/소프트웨어 내부구조를 분석</td>
    </tr>
    <tr>
        <td>주로 개발단계에서 수행</td>
    </tr>
    <tr>
        <td>소프트웨어 내부 구조와 동작 검증에 집중</td>
    </tr>
</table>

#### 테스트 설계 기법의 구분
> 테스트 설계의 근원을 기준

<table>
    <tr>
        <td rowspan="3">동적 테스트</td>
        <td>명세 기반 기법(Specification Based)</td>
        <td>테스트 베이시스 분석을 통한 Test Case 설계</td>
    </tr>
    <tr>
        <td>구조 기반 기법(Structure Based)</td>
        <td>소스 코드/모델 등 구현정보를 기반으로 Test Case 설계</td>
    </tr>
    <tr>
        <td>경험기반 기법(Experience Based) + 추가적</td>
        <td>개발자/테스터의 지식이나 경험을 기반으로 Test Case 설계</td>
    </tr>
</table>
