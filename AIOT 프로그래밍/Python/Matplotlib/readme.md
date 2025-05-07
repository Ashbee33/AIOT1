# 📊 Matplotlib 기본 문법 정리

`matplotlib`은 파이썬에서 데이터를 시각화할 수 있는 대표적인 라이브러리입니다. 그중에서도 `pyplot` 모듈은 간단하고 직관적인 인터페이스를 제공합니다.

---

## 1. matplotlib 임포트

```python
import matplotlib.pyplot as plt
```

---

## 2. 기본 선 그래프 (Line Plot)

```python
x = [1, 2, 3, 4, 5]
y = [10, 14, 19, 23, 28]

plt.plot(x, y)
plt.title("선 그래프")
plt.xlabel("x축")
plt.ylabel("y축")
plt.show()
```

---

## 3. 마커, 선, 색 지정

```python
plt.plot(x, y, marker='o', linestyle='--', color='r')
# marker: 'o', '^', 's' 등
# linestyle: '-', '--', '-.', ':'
# color: 'r', 'g', 'b', 'k' 등
plt.show()
```

---

## 4. 여러 그래프 그리기

```python
x = [1, 2, 3, 4, 5]
y1 = [10, 20, 30, 40, 50]
y2 = [5, 15, 25, 35, 45]

plt.plot(x, y1, label='선 1')
plt.plot(x, y2, label='선 2')
plt.legend()
plt.show()
```

---

## 5. 막대 그래프 (Bar Chart)

```python
categories = ['A', 'B', 'C', 'D']
values = [10, 20, 15, 25]

plt.bar(categories, values)
plt.title("막대 그래프")
plt.show()
```

---

## 6. 수평 막대 그래프

```python
plt.barh(categories, values)
plt.title("수평 막대 그래프")
plt.show()
```

---

## 7. 히스토그램 (Histogram)

```python
data = [1, 1, 2, 2, 2, 3, 3, 4, 5, 5, 5, 5, 6]

plt.hist(data, bins=5)
plt.title("히스토그램")
plt.xlabel("값")
plt.ylabel("빈도수")
plt.show()
```

---

## 8. 산점도 (Scatter Plot)

```python
x = [1, 2, 3, 4, 5]
y = [5, 7, 4, 6, 8]

plt.scatter(x, y)
plt.title("산점도")
plt.show()
```

---

## 9. 파이 차트 (Pie Chart)

```python
labels = ['사과', '바나나', '체리', '포도']
sizes = [30, 25, 25, 20]

plt.pie(sizes, labels=labels, autopct='%1.1f%%')
plt.title("과일 비율")
plt.show()
```

---

## 10. 그래프 저장하기

```python
plt.plot([1, 2, 3], [4, 5, 6])
plt.savefig("graph.png")  # 그래프를 PNG로 저장
```

---

## 11. 서브플롯 (여러 그래프 나란히 출력)

```python
plt.subplot(1, 2, 1)  # 1행 2열 중 첫 번째
plt.plot([1, 2, 3], [1, 4, 9])
plt.title("첫 번째 그래프")

plt.subplot(1, 2, 2)  # 1행 2열 중 두 번째
plt.plot([1, 2, 3], [9, 4, 1])
plt.title("두 번째 그래프")

plt.tight_layout()  # 레이아웃 자동 조정
plt.show()
```

---

## 12. 한글 폰트 설정 (예: Windows 환경)

```python
import matplotlib.pyplot as plt
plt.rcParams['font.family'] = 'Malgun Gothic'  # Windows: 'Malgun Gothic', macOS: 'AppleGothic'
plt.rcParams['axes.unicode_minus'] = False     # 음수 기호 깨짐 방지
```

---

> ✅ **팁:** `matplotlib`은 `numpy`, `pandas`와 함께 자주 사용되며, 시각화를 통해 데이터를 더 효과적으로 분석하고 전달할 수 있게 도와줍니다.

