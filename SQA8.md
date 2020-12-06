### 유즈 케이스 테스팅(Use Case Testing)
> 유스케이스나 비지니스 시나리오를 기반으로 TC를 도출하는 테스트 설계 기법
    - 대개 주류 시나리오/기본 흐름(MainStream Scenario, Basic or Main flow)과 대체 흐름(Alternative branches or Alternative flows)으로 구성
    - 각각의 유스케이스는 유스케이스 명세(Use Case descrption)를 포함</br>

- 유스 케이스 명세서
    - 시스템이 제공하는 기본단위 기능, 즉 유스케이스와 액터(사용자 및 시스템)간이 상호작용을 정의

    ![유스 케이스](https://lh3.googleusercontent.com/proxy/Ua1v2RVvB3_UGjf0TQaoUvAODphL829EPFl-nOuSYc-P7FV_AmedM3xKW2JaXAFLoFuImadRQ9IVxUx1_pCucGDhChzNiBBuC75841A_ImEWrg)

- 요구 사항 시나리오 분석을 통해 유스케이스 TC를 추출
- 요구 사항을 통과하는 모든 경로를 조합하면, 서로다른 요구사항 시나리오를 만들 수 있다.
- 단, 반복은 한번만 수행된다고 가정한다. (Alternative 3 = single loop)

![](https://flylib.com/books/1/558/1/html/2/files/15fig05.gif)

<table>
    <tr>
        <td>종류</td>
        <td colspan="3">Flow</td>
    </tr>
    <tr>
        <td>Scenario 1</td>
        <td>Basic Flow</td>
        <td>-</td>
        <td>-</td>
    </tr>
    <tr>
        <td>Scenario 2</td>
        <td>Basic Flow</td>
        <td>Alternative Flow 1</td>
        <td>-</td>
    </tr>
    <tr>
        <td>Scenario 3</td>
        <td>Basic Flow</td>
        <td>Alternative Flow 1</td>
        <td>Alternative Flow 2</td>
    </tr>
    <tr>
        <td>Scenario 4</td>
        <td>Basic Flow</td>
        <td>Alternative Flow 3</td>
        <td>Alternative Flow 1</td>
    </tr>
    <tr>
        <td>......</td>
        <td>......</td>
        <td>......</td>
        <td>......</td>
    </tr>
</table>

### 페어 와이즈 테스팅 기법(Pair-wise Testing)
> 쌍, 조합 → TC 조합하는 방법

- 커버해야할 기능적 범위에 비해 상대적으로 적은 양의 테스트 세트를 구성
- 대부분의 결함이 2개의 요소의 상호작용(interaction of two factors)에 기인한다는 것을 착안</br>
    - 2개 요소의 모든 조합을 TC로 도출
- 하나으 ㅣ파라미터의 각 값들이 모든 파라미터의 각 값들과 최소 한번씩 조합이 되는 집합