# 🐍 파이썬(Python) 기본 문법 정리

파이썬은 초보자도 배우기 쉬운 구조를 가진 범용 프로그래밍 언어입니다. 아래는 주요 기본 문법을 하나로 정리한 내용입니다.

## 1. 출력
```python
print("Hello, World!")
```

## 2. 변수와 자료형
```python
x = 10          # 정수
y = 3.14        # 실수
name = "Alice"  # 문자열
is_on = True    # 불리언 (True 또는 False)
```

## 3. 연산자
```python
a = 5 + 2     # 덧셈: 7
b = 5 - 2     # 뺄셈: 3
c = 5 * 2     # 곱셈: 10
d = 5 / 2     # 나눗셈: 2.5
e = 5 // 2    # 정수 나눗셈: 2
f = 5 % 2     # 나머지: 1
g = 2 ** 3    # 거듭제곱: 8
```

## 4. 조건문
```python
x = 10
if x > 5:
    print("x는 5보다 큽니다.")
elif x == 5:
    print("x는 5입니다.")
else:
    print("x는 5보다 작습니다.")
```

## 5. 반복문
```python
# for문
for i in range(5):  # 0부터 4까지 반복
    print(i)

# while문
count = 0
while count < 5:
    print(count)
    count += 1
```

## 6. 리스트(List)
```python
fruits = ["apple", "banana", "cherry"]
print(fruits[1])       # banana
fruits.append("grape") # 리스트에 항목 추가
```

## 7. 함수 정의
```python
def greet(name):
    print("Hello,", name)

greet("Alice")
```

## 8. 딕셔너리(Dictionary)
```python
person = {"name": "Alice", "age": 25}
print(person["name"])       # Alice
person["age"] = 26          # 값 수정
```

## 9. 클래스와 객체
```python
class Person:
    def __init__(self, name):
        self.name = name

    def greet(self):
        print("Hello, my name is", self.name)

p = Person("Alice")
p.greet()
```

## 10. 예외 처리
```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("0으로 나눌 수 없습니다.")
finally:
    print("프로그램 종료")
```

> ✅ **들여쓰기 주의!** 파이썬은 들여쓰기가 문법의 일부입니다. 같은 블록의 코드는 반드시 같은 수준으로 들여써야 합니다.

