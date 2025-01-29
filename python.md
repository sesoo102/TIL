### 📝 **SSAFY Python 핵심 노트 (1월 20일 ~ 1월 24일)**
> 🔥 **이 노트는 SSAFY 수업 내용을 바탕으로 핵심 개념을 정리하고, 단계적인 설명과 예제 문제를 포함합니다.**  
**각 날짜별로 중요한 개념을 배우고 복습할 수 있도록 구성했습니다.**  
**📅 1월 20일 ~ 1월 24일까지의 내용을 정리한 핵심 노트입니다.**  

---

## **📌 1월 20일 (Python 기본 문법, 변수와 데이터 타입)**
### 1️⃣ **변수(Variable)와 데이터 타입**
- **변수:** 데이터를 저장하는 공간 (이름을 할당하여 접근)
- **변수 할당 방식**
  ```python
  x = 10  # 정수 변수
  name = "Alice"  # 문자열 변수
  pi = 3.14  # 실수 변수
  ```
- **데이터 타입**
  | 타입 | 설명 |
  |------|------|
  | `int` | 정수형 |
  | `float` | 실수형 |
  | `str` | 문자열 |
  | `list` | 리스트 (가변) |
  | `tuple` | 튜플 (불변) |
  | `dict` | 딕셔너리 (Key-Value 저장) |
  | `set` | 집합 (중복 제거) |
  | `bool` | 참(`True`), 거짓(`False`) |

### 2️⃣ **연산자**
- **산술 연산자** `+`, `-`, `*`, `/`, `//`, `%`, `**`
- **비교 연산자** `==`, `!=`, `>`, `<`, `>=`, `<=`
- **논리 연산자** `and`, `or`, `not`

#### 📝 **예제 문제**
```python
# 주어진 정수 num이 짝수인지 홀수인지 판별하여 출력하는 프로그램을 작성하세요.
num = int(input("정수를 입력하세요: "))
if num % 2 == 0:
    print("짝수입니다.")
else:
    print("홀수입니다.")
```

---

## **📌 1월 21일 (자료형: 문자열, 리스트, 튜플, 딕셔너리, 집합)**
### 1️⃣ **문자열 (String)**
- 문자열 조작 메서드
  ```python
  text = "hello world"
  print(text.upper())  # HELLO WORLD
  print(text.replace("hello", "hi"))  # hi world
  print(text.split())  # ['hello', 'world']
  ```
- 문자열 인덱싱과 슬라이싱
  ```python
  text = "Python"
  print(text[0])  # P
  print(text[-1]) # n
  print(text[0:3]) # Pyt (슬라이싱)
  ```

### 2️⃣ **리스트 (List)**
- **리스트 메서드**
  ```python
  numbers = [1, 2, 3]
  numbers.append(4)  # [1, 2, 3, 4]
  numbers.pop()  # [1, 2, 3]
  numbers.sort()  # 정렬
  numbers.reverse()  # 역순 정렬
  ```

### 3️⃣ **딕셔너리 (Dictionary)**
- **Key-Value 저장**
  ```python
  student = {"name": "Alice", "age": 20}
  print(student["name"])  # Alice
  student["major"] = "Computer Science"
  ```

### 4️⃣ **집합 (Set)**
- 중복 제거, 집합 연산 (`|`, `&`, `-`)
  ```python
  set1 = {1, 2, 3}
  set2 = {3, 4, 5}
  print(set1 | set2)  # 합집합 {1, 2, 3, 4, 5}
  print(set1 & set2)  # 교집합 {3}
  print(set1 - set2)  # 차집합 {1, 2}
  ```

#### 📝 **예제 문제**
```python
# 리스트에서 중복을 제거하고 정렬된 리스트를 반환하는 함수 작성
def remove_duplicates(lst):
    return sorted(list(set(lst)))

nums = [4, 2, 1, 2, 3, 4]
print(remove_duplicates(nums))  # [1, 2, 3, 4]
```

---

## **📌 1월 22일 (함수, 매개변수, return, 내장 함수)**
### 1️⃣ **함수 정의와 호출**
- **기본 함수**
  ```python
  def greet(name):
      print(f"Hello, {name}!")
      
  greet("Alice")  # Hello, Alice!
  ```
- **매개변수와 인자**
  ```python
  def add(a, b=10):  # 기본값 설정
      return a + b

  print(add(5))  # 15
  print(add(5, 3))  # 8
  ```
- **가변 인자 (`*args`, `**kwargs`)**
  ```python
  def total(*args):
      return sum(args)

  print(total(1, 2, 3, 4))  # 10
  ```

#### 📝 **예제 문제**
```python
# 숫자의 팩토리얼을 구하는 재귀 함수 구현
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)

print(factorial(5))  # 120
```

---

## **📌 1월 23일 (모듈, 제어문: 조건문, 반복문)**
### 1️⃣ **모듈 사용하기**
- **모듈 불러오기**
  ```python
  import math
  print(math.sqrt(16))  # 4.0
  ```
- **사용자 정의 모듈**
  ```python
  # my_module.py
  def add(a, b):
      return a + b
  ```
  ```python
  # main.py
  import my_module
  print(my_module.add(3, 5))  # 8
  ```

### 2️⃣ **제어문**
- **조건문 (if)**
  ```python
  score = 85
  if score >= 90:
      print("A")
  elif score >= 80:
      print("B")
  else:
      print("C")
  ```
- **반복문 (for, while)**
  ```python
  for i in range(1, 6):
      print(i)  # 1 2 3 4 5
  ```

#### 📝 **예제 문제**
```python
# 1부터 100까지의 숫자 중에서 3의 배수만 출력하는 프로그램을 작성하세요.
for i in range(1, 101):
    if i % 3 == 0:
        print(i)
```

---

## **📌 1월 24일 (데이터 구조, 리스트/딕셔너리 활용)**
### 1️⃣ **리스트 조작**
- **리스트 컴프리헨션**
  ```python
  squares = [x**2 for x in range(10)]
  print(squares)  # [0, 1, 4, 9, ..., 81]
  ```

### 2️⃣ **딕셔너리 활용**
- **딕셔너리 컴프리헨션**
  ```python
  keys = ['name', 'age']
  values = ['Alice', 25]
  student = {k: v for k, v in zip(keys, values)}
  ```

#### 📝 **예제 문제**
```python
# 리스트를 받아 짝수만 남기는 함수 작성
def filter_even(lst):
    return [x for x in lst if x % 2 == 0]

print(filter_even([1, 2, 3, 4, 5, 6]))  # [2, 4, 6]
```

---
