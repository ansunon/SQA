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


### ② 경계값 분석(Boundary Value Anaysis)