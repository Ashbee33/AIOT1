# 🌊 Seaborn 기본 문법 정리

`seaborn`은 `matplotlib` 기반의 고급 시각화 라이브러리로, 통계적 데이터 시각화에 유용하며 `pandas` DataFrame과 잘 연동됩니다.

---

## 1. seaborn 임포트

```python
import seaborn as sns
import matplotlib.pyplot as plt
```

---

## 2. 예제 데이터셋 로드

```python
df = sns.load_dataset("titanic")  # 내장 데이터셋 (예: 타이타닉 생존자 데이터)
df.head()
```

---

## 3. 스타일 설정

```python
sns.set_style("whitegrid")  # "darkgrid", "white", "ticks" 등
```

---

## 4. 기본 그래프 종류

### ① 산점도 (Scatter Plot)

```python
sns.scatterplot(x='age', y='fare', data=df)
plt.title("산점도")
plt.show()
```

---

### ② 선 그래프 (Line Plot)

```python
sns.lineplot(x='age', y='fare', data=df)
```

---

### ③ 막대 그래프 (Bar Plot)

```python
sns.barplot(x='sex', y='survived', data=df)
```

---

### ④ 카운트 플롯 (Count Plot)

```python
sns.countplot(x='class', data=df)
```

---

### ⑤ 히스토그램 + KDE (displot)

```python
sns.displot(df['age'], kde=True, bins=20)
```

---

### ⑥ 박스 플롯 (Box Plot)

```python
sns.boxplot(x='class', y='age', data=df)
```

---

### ⑦ 바이올린 플롯 (Violin Plot)

```python
sns.violinplot(x='class', y='age', data=df)
```

---

### ⑧ 히트맵 (Heatmap)

```python
corr = df.corr(numeric_only=True)
sns.heatmap(corr, annot=True, cmap='coolwarm')
```

---

## 5. 그룹별 시각화

```python
sns.barplot(x='sex', y='survived', hue='class', data=df)
```

---

## 6. 페어플롯 (변수 간 관계 전체 시각화)

```python
sns.pairplot(df[['age', 'fare', 'survived']])
```

---

## 7. 조인트플롯 (이변량 분석)

```python
sns.jointplot(x='age', y='fare', data=df, kind='hex')
```

---

## 8. 카테고리별 정렬

```python
sns.boxplot(x='embark_town', y='fare', data=df, order=['Southampton', 'Cherbourg', 'Queenstown'])
```

---

## 9. 저장 및 출력

```python
plt.savefig('seaborn_plot.png')
plt.show()
```

---

> ✅ **TIP:** Seaborn은 기본 통계 처리가 내장되어 있어 복잡한 시각화도 짧은 코드로 구현할 수 있습니다. `pandas`와 함께 사용할 때 매우 강력한 도구입니다.

