# 🐍 Numpy 패키지 기본 문법

Numpy는 고성능 수치 계산을 위한 파이썬 라이브러리로, 다차원 배열 객체인 `ndarray`와 이를 다루기 위한 다양한 수학적 함수들을 제공합니다.

## 1. Numpy 패키지 임포트
```python
import numpy as np
```

## 2. 배열 생성

### 2.1. 리스트를 배열로 변환
```python
arr = np.array([1, 2, 3, 4, 5])
print(arr)  # 출력: [1 2 3 4 5]
```

### 2.2. 2D 배열 생성
```python
arr_2d = np.array([[1, 2], [3, 4], [5, 6]])
print(arr_2d)
# 출력:
# [[1 2]
#  [3 4]
#  [5 6]]
```

### 2.3. `zeros()` 배열 생성
```python
arr_zeros = np.zeros((3, 4))  # 3x4 크기의 0 배열 생성
print(arr_zeros)
# 출력:
# [[0. 0. 0. 0.]
#  [0. 0. 0. 0.]
#  [0. 0. 0. 0.]]
```

### 2.4. `ones()` 배열 생성
```python
arr_ones = np.ones((2, 3))  # 2x3 크기의 1 배열 생성
print(arr_ones)
# 출력:
# [[1. 1. 1.]
#  [1. 1. 1.]]
```

### 2.5. `arange()` 배열 생성
```python
arr_arange = np.arange(0, 10, 2)  # 0부터 10까지 2씩 증가
print(arr_arange)  # 출력: [0 2 4 6 8]
```

### 2.6. `linspace()` 배열 생성
```python
arr_linspace = np.linspace(0, 1, 5)  # 0과 1 사이를 5개 구간으로 나누어 배열 생성
print(arr_linspace)
# 출력: [0.   0.25 0.5  0.75 1.  ]
```

## 3. 배열 속성

### 3.1. 배열의 차원 확인
```python
arr = np.array([1, 2, 3])
print(arr.ndim)  # 출력: 1 (1차원)
```

### 3.2. 배열의 형태 확인
```python
arr_2d = np.array([[1, 2], [3, 4]])
print(arr_2d.shape)  # 출력: (2, 2) (2x2 배열)
```

### 3.3. 배열의 크기 확인
```python
print(arr_2d.size)  # 출력: 4 (4개의 원소)
```

## 4. 배열 연산

### 4.1. 기본 연산
```python
arr = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])

print(arr + arr2)  # 출력: [5 7 9]
print(arr * arr2)  # 출력: [ 4 10 18]
```

### 4.2. 스칼라와의 연산
```python
arr = np.array([1, 2, 3])
print(arr + 2)  # 출력: [3 4 5]
print(arr * 2)  # 출력: [2 4 6]
```

### 4.3. 배열의 요소별 연산
```python
arr = np.array([1, 2, 3])
print(np.sin(arr))  # 출력: [0.84147098 0.90929743 0.14112001] (각 요소의 사인값)
```

## 5. 배열 인덱싱

### 5.1. 1D 배열 인덱싱
```python
arr = np.array([10, 20, 30, 40, 50])
print(arr[0])  # 출력: 10
print(arr[-1])  # 출력: 50 (마지막 원소)
```

### 5.2. 2D 배열 인덱싱
```python
arr_2d = np.array([[1, 2], [3, 4], [5, 6]])
print(arr_2d[1, 0])  # 출력: 3 (2번째 행, 1번째 열)
print(arr_2d[:, 1])   # 출력: [2 4 6] (모든 행, 2번째 열)
```

### 5.3. 조건을 이용한 인덱싱
```python
arr = np.array([1, 2, 3, 4, 5])
print(arr[arr > 2])  # 출력: [3 4 5] (3보다 큰 값)
```

## 6. 배열 결합

### 6.1. `vstack()` (수직 결합)
```python
arr1 = np.array([1, 2])
arr2 = np.array([3, 4])
result = np.vstack((arr1, arr2))
print(result)
# 출력:
# [[1 2]
#  [3 4]]
```

### 6.2. `hstack()` (수평 결합)
```python
arr1 = np.array([1, 2])
arr2 = np.array([3, 4])
result = np.hstack((arr1, arr2))
print(result)  # 출력: [1 2 3 4]
```

## 7. 배열 연산 함수

### 7.1. `sum()`
```python
arr = np.array([1, 2, 3])
print(arr.sum())  # 출력: 6 (배열의 합)
```

### 7.2. `mean()`
```python
arr = np.array([1, 2, 3])
print(arr.mean())  # 출력: 2.0 (배열의 평균)
```

### 7.3. `max()`와 `min()`
```python
arr = np.array([1, 2, 3])
print(arr.max())  # 출력: 3 (최대값)
print(arr.min())  # 출력: 1 (최소값)
```

---

Numpy는 배열 연산뿐만 아니라 많은 수학적, 통계적 함수들을 제공하여 다양한 과학적 계산에 사용됩니다. 위에서 설명한 기본 문법을 통해 Numpy를 활용할 수 있습니다.

