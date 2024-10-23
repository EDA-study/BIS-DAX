# INT

- 입력 받은 숫자를 가장 가까운 정수로 내림 합니다.

## 문법

```
INT(<숫자>)
```

## 매개변수

매개변수 명 | 설명 
---------|----------
 숫자 | 정수로 내림 시키고자 하는 숫자


## 반환 결과

- <숫자>를 내림하여 산출된 정수

## 실습 문제

> 아래 조건으로 `<날씨>` 테이블에 새 열(계산된 열)을 추가하시오.

- 새 열 이름: `[정수_평균기온]`
- 활용 필드: `<날씨>` 테이블의 `[평균기온]` 필드
- 새 열 설명: 행별 `[평균기온]`을 가장 가까운 정수로 내림한 값
- 사용 함수: `INT`

### 선택지

A. 
```
[정수_평균기온] = INT('날씨'[평균기온])
```

B. 
```
[정수_평균기온] = INT(SUM('날씨'[평균기온]))
```

### 정답 및 해설

```{admonition} 클릭해서 정답 및 해설을 확인해보세요.
:class: dropdown

정답: A

A. INT 함수를 사용한 후 <날씨> 테이블에 있는 [평균기온] 필드를 인자로 입력했음. 새 열 특성상 행 별로 들어가 있는 숫자들이 INT 함수에 전달되기 때문에 정상적인 문법. 그러므로 정답.

B. SUM 함수를 요구하지 않았음. 그와 더불어 위 문법은 SUM 함수를 사용해 [평균기온] 필드내에 있는 모든 기온의 합을 먼저 구하고, 그 합에 대해 내림하여 정수를 구함. 결론적으로 생성되는 [정수_평균기온] 필드에는 모든 행에 동일한 상수가 들어감. 문제에서 요구하는 행별로 정수 값이 계산되지 않음. 그러므로 오답.

```