# 🐼 Pandas 패키지 기본 문법

Pandas는 데이터 분석과 처리에 특화된 파이썬 라이브러리입니다. 표 형태의 데이터(`DataFrame`)와 1차원 데이터(`Series`)를 쉽게 다룰 수 있습니다.

## 1. pandas 임포트
```python
import pandas as pd
```

---

## 2. Series 생성
```python
s = pd.Series([10, 20, 30, 40])
print(s)
```

### Series는 1차원 배열로, 인덱스와 값으로 구성됩니다.

---

## 3. DataFrame 생성

### 리스트로 생성
```python
data = [[1, 'Alice'], [2, 'Bob'], [3, 'Charlie']]
df = pd.DataFrame(data, columns=['ID', 'Name'])
print(df)
```

### 딕셔너리로 생성
```python
data = {'Name': ['Alice', 'Bob', 'Charlie'], 'Age': [25, 30, 35]}
df = pd.DataFrame(data)
print(df)
```

---

## 4. 데이터 불러오기

```python
df = pd.read_csv('data.csv')        # CSV 파일 읽기
df = pd.read_excel('data.xlsx')     # Excel 파일 읽기
df.to_csv('output.csv', index=False)  # CSV로 저장
```

---

## 5. DataFrame 기본 정보

```python
df.head()       # 상위 5개 행
df.tail()       # 하위 5개 행
df.shape        # (행, 열)
df.columns      # 열 이름
df.index        # 행 인덱스
df.info()       # 요약 정보
df.describe()   # 기초 통계 요약
```

---

## 6. 열 및 행 접근

### 열 접근
```python
df['Name']             # 단일 열
df[['Name', 'Age']]    # 여러 열
```

### 행 접근
```python
df.loc[0]              # 라벨 기반 인덱싱
df.iloc[0]             # 정수 위치 기반 인덱싱
```

---

## 7. 조건 필터링
```python
df[df['Age'] > 30]             # Age가 30 초과인 행
df[(df['Age'] > 25) & (df['Name'] == 'Bob')]  # 다중 조건
```

---

## 8. 값 수정
```python
df.loc[0, 'Age'] = 26      # 특정 셀 수정
df['Age'] = df['Age'] + 1  # 열 전체 수정
```

---

## 9. 결측치 처리

```python
df.isnull()              # 결측치 여부 확인
df.dropna()              # 결측치가 있는 행 제거
df.fillna(0)             # 결측치 0으로 채우기
```

---

## 10. 정렬
```python
df.sort_values(by='Age')            # Age 기준 오름차순
df.sort_values(by='Age', ascending=False)  # 내림차순
```

---

## 11. 그룹화 (GroupBy)

```python
df.groupby('Name')['Age'].mean()    # 이름별 평균 나이
```

---

## 12. 열 추가 및 삭제

```python
df['NewCol'] = df['Age'] * 2        # 새 열 추가
df.drop(columns=['NewCol'], inplace=True)  # 열 삭제
```

---

## 13. 중복 제거
```python
df.drop_duplicates()
```

---

## 14. 데이터 병합 및 연결

### concat (행 또는 열 방향 연결)
```python
df_new = pd.concat([df1, df2], axis=0)  # 행 방향 연결
```

### merge (공통 열 기준 병합)
```python
df_merged = pd.merge(df1, df2, on='ID')  # ID 기준 병합
```

---

## 15. 날짜 처리

```python
df['Date'] = pd.to_datetime(df['Date'])
df['Year'] = df['Date'].dt.year
df['Month'] = df['Date'].dt.month
```

---

> ✅ Pandas는 데이터 분석에서 가장 많이 사용하는 라이브러리 중 하나이며, 다양한 파일 형식 지원, 시계열 처리, 통계 계산 등에 매우 유용합니다.

