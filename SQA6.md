### 명세 기반 기법
#### ① 동등 분할(Equivalence partitioning)
- 입력값/출력값 영역(Input/Output space)을 유한개의 상호 독립적인 집합(Mutual disjoint subset)으로 분할하여 각 집합의 원소중 대표값 하나를 선택해 테스트 케이스를 선정
- 동일 집합에서 어떤 대표값을 사용하더라도 같은 결과를 나타낼 것이라 기대
- 유효한 입력 데이터와 유효하지 않은입력 데이터를(입력되지 말아야할 값) 포함할수 있다.

![동등 분할](https://www.guru99.com/images/3-2016/032316_0620_Equivalence5.png)


<table>
    <tr>
        <td>종류</td>
        <td colspan="2">Valid Input</td>
        <td colspan="2">InValid Input</td>
    </tr>
    <tr>
        <td>경계값(Boundary value)</td>
        <td>경계값 내부</td>
        <td>1 개</td>
        <td>경계 밖의 값</td>
        <td>1 개</td>
    </tr>
    <tr>
        <td>불리언(Boolean)</td>
        <td>True</td>
        <td>1 개</td>
        <td>False</td>
        <td>1 개</td>
    </tr>
    <tr>
        <td>범위(Range)</td>
        <td>범위 내부</td>
        <td>1 개</td>
        <td>범위 밖의 값(양방향)</td>
        <td>2 개</td>
    </tr>
    <tr>
        <td>숫자(Number)</td>
        <td>숫자</td>
        <td>1 개</td>
        <td>작은 수, 큰수</td>
        <td>2 개</td>
    </tr>
    <tr>
        <td>값의 집합(Set of values)</td>
        <td>집합 내의 값</td>
        <td>1 개</td>
        <td>집합에 없는 값</td>
        <td>1 개</td>
    </tr>
</table>


#### ② 경계값 분석(Boundary Value Anaysis)
> 입력값의 주요 오류 대상인 경계값을 테스트 데이터로 선정하는 기법
- 경험적으로 개발자가 경계값 처리시 오류 발생 가능성이 높기 때문에 경계값 주변값을 위주로 분석
- 경계값: 해당 분할 영역의 최대값과 최소값(유효 경계값/ 비유효 경계값 등)
- Boolean 값은 적절하지 않음
> 동등 Class 식별 ▶ 엽력값 경계 식별 ▶ 경계값 설정 ▶ Test Case 작성</br>

- 경계값 선택 기준
> Equivalence Class 를 찾은 후 대표값을 선택할 때 경계값과 그 전후의 값들을 사용한다.

![경계값 분석](https://e7.pngegg.com/pngimages/442/750/png-clipart-black-box-testing-software-testing-boundary-value-analysis-white-box-testing-equivalence-partitioning-text-edit-box-angle-text.png)

- 등가 분할 및 경계값 분석 기법의 한계점
    - 일련의 동작에 대한 조합을 테스트하기에는 적합하지 않다.
    - 입력 범위를 동등분할하여 제한하더라도 입력값 조합의 수가 테스트 가능한 수를 넘어서는 경우가 많다.
    - 입력 조합이 상호간에 독립적(의존성 없는)이라는 가정에서만 적합한 기법이다.
    - 출력이 입력 조건이나 변수들 사이의 관계에 따라 달라지는 경우, 입력조건을 동등분할 하는 것이 매우 어려울 수 있다.