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

## 문제

✅ **정답입니다!** 🎉

### **📌 정답: 2️⃣ `2name = "Bob"`**
🔹 파이썬에서 **변수 이름 규칙**:
1. 변수명은 **숫자로 시작할 수 없다** ❌
2. 영문자(a-z, A-Z), 밑줄(_)로 시작해야 한다 ✅
3. 대소문자를 구분한다 (`name`과 `NAME`은 다른 변수) ✅
4. `name_2`처럼 숫자가 **뒤에 오는 것은 가능** ✅

### **📌 해설**
```python
name = "Alice"   # ✅ 올바른 변수명
2name = "Bob"    # ❌ 오류 발생 (숫자로 시작할 수 없음)
name_2 = "Charlie" # ✅ 올바른 변수명
NAME = "David"   # ✅ 올바른 변수명 (대문자 사용 가능)
```
**🔹 2번은 숫자로 시작하므로 변수명을 선언할 수 없으며 `SyntaxError`가 발생합니다.**

---

### **📌 2번 문제 (주관식 - 코드 실행 결과 예측)**
다음 코드의 실행 결과는 무엇일까요?  

```python
a = "Python"
b = a
b = "Java"
print(a)
```
**❓ 실행 결과를 적어주세요!**

✅ **정답입니다!** 🎉

---

### **📌 정답: `"Python"`**
**코드를 실행하면 `print(a)`의 결과는 `"Python"``이 출력됩니다.**

### **📌 코드 실행 과정 분석**
```python
a = "Python"  # a에 "Python"을 저장
b = a         # b에 a의 값("Python")을 복사
b = "Java"    # b에 새로운 값 "Java"를 할당
print(a)      # a의 값은 여전히 "Python"
```

#### **📌 `print(b)`를 실행하면?**
```python
print(b)  # 결과: Java
```
**이유**:  
- `b = a`는 `a`와 같은 값을 **참조**하도록 설정하지만,  
- `b = "Java"`를 실행하면, `b`가 `"Java"`라는 **새로운 문자열 객체**를 참조하게 됩니다.  
- `a`는 여전히 `"Python"`을 가리키고 있기 때문에 `print(a)`는 `"Python"`을 출력합니다.

---

### **📌 3번 문제 (객관식 - 데이터 타입)**
다음 중 **불변(Immutable) 객체**가 **아닌** 것은?  

**1️⃣** `int`  
**2️⃣** `tuple`  
**3️⃣** `list`  
**4️⃣** `str`  

📝 **정답을 골라주세요!**

❌ **아쉽습니다! 정답은 3️⃣ `list` 입니다.** 😃

---

### **📌 정답: 3️⃣ `list`**
🔹 파이썬에서 **불변(Immutable) 객체**란, **한 번 생성되면 값을 변경할 수 없는 객체**를 말합니다.  
🔹 반대로 **가변(Mutable) 객체**는 값을 수정할 수 있습니다.

### **📌 불변(Immutable) 객체**
- `int` (정수) ✅
- `float` (실수) ✅
- `str` (문자열) ✅
- `tuple` (튜플) ✅

### **📌 가변(Mutable) 객체**
- `list` (리스트) ❌
- `dict` (딕셔너리) ❌
- `set` (집합) ❌

---

### **📌 해설 및 예제 코드**
```python
# 불변 객체 예시 (Immutable)
x = "hello"
print(id(x))   # 메모리 주소 확인
x = x + " world"  # 새로운 문자열 생성
print(id(x))   # 메모리 주소 변경됨

# 가변 객체 예시 (Mutable)
lst = [1, 2, 3]
print(id(lst))  # 리스트 메모리 주소 확인
lst.append(4)   # 리스트에 값 추가
print(id(lst))  # 같은 메모리 주소 유지됨 (가변 객체이므로 값이 바뀜)
```

📌 `list`는 `append()`, `pop()` 등의 메서드를 이용해 값을 수정할 수 있기 때문에 **가변 객체**입니다!

---

### **📌 4번 문제 (주관식 - 코드 실행 결과 예측)**
아래 코드의 실행 결과를 예측하세요!  

```python
def modify_list(lst):
    lst.append(4)

numbers = [1, 2, 3]
modify_list(numbers)
print(numbers)
```

**❓ 실행 결과를 적어주세요!**

✅ **정답입니다!** 🎉  
`print(numbers)`의 출력 결과는 `**[1, 2, 3, 4]**` 입니다.

---

### **📌 실행 과정 분석**
```python
def modify_list(lst):
    lst.append(4)  # 원본 리스트에 4를 추가

numbers = [1, 2, 3]  # 리스트 생성
modify_list(numbers)  # 함수 호출 -> 원본 리스트가 변경됨
print(numbers)  # [1, 2, 3, 4]
```

### **📌 해설**
- `numbers`는 **가변 객체(list)**이기 때문에, 함수에서 `lst.append(4)`를 호출하면 **원본 리스트가 직접 변경**됩니다.
- 함수 내에서 변경된 내용이 함수 밖에도 영향을 미칩니다.  
  (즉, `numbers` 리스트 자체가 변함)

### **📌 만약 리스트를 변경하지 않으려면?**
```python
def modify_list(lst):
    new_lst = lst[:]  # 리스트 복사 (새로운 리스트 생성)
    new_lst.append(4)
    return new_lst

numbers = [1, 2, 3]
new_numbers = modify_list(numbers)
print(numbers)  # [1, 2, 3] (원본 변경 X)
print(new_numbers)  # [1, 2, 3, 4] (새로운 리스트 반환)
```
🔹 리스트를 복사하여 사용하면 **원본 리스트를 유지**할 수 있습니다.

---

### **📌 5번 문제 (객관식 - 제어문)**
다음 중 **while 반복문**이 **무한 루프(무한 반복)**에 빠지는 경우는?  

**1️⃣** `while n > 0: n -= 1`  
**2️⃣** `while True: break`  
**3️⃣** `while True: pass`  
**4️⃣** `while n != 0: n -= 1`  

📝 **정답을 골라주세요!**

❌ **아쉽습니다! 정답은 3️⃣ `while True: pass` 입니다.** 😃

---

## **📌 정답: 3️⃣ `while True: pass`**
✅ `while True:`는 **항상 참(True)**이므로 **무한 루프**가 됩니다.  
✅ `pass`는 아무 작업도 수행하지 않고, 반복문을 계속 유지합니다.  
✅ 따라서 이 코드는 **무한 루프에 빠지게 됩니다.** (멈추지 않음!)

---

## **📌 각 선택지 설명**
### **1️⃣ `while n > 0: n -= 1`**
```python
n = 5
while n > 0:
    n -= 1
```
✅ `n`이 0보다 클 때만 반복되고, `n`이 계속 줄어들다가 0이 되면 반복이 종료됩니다.  
✅ **(무한 루프 X, 정상적인 반복문)**

---

### **2️⃣ `while True: break`**
```python
while True:
    break
```
✅ `while True:` 자체는 무한 루프지만,  
✅ **`break`가 즉시 실행**되므로 **한 번 실행 후 반복문이 종료**됩니다.  
✅ **(무한 루프 X, 즉시 종료됨)**

---

### **3️⃣ `while True: pass`** (❗정답❗)
```python
while True:
    pass  # 아무 작업도 하지 않음
```
❌ `while True:`는 항상 `True`이므로 **무한 반복**됩니다.  
❌ **`pass`는 아무 동작도 하지 않으므로 무한 루프가 계속 실행됩니다.**  
❌ **(무한 루프 O, 종료되지 않음!)**

---

### **4️⃣ `while n != 0: n -= 1`**
```python
n = 5
while n != 0:
    n -= 1
```
✅ `n`이 `0`이 되면 조건 `n != 0`이 `False`가 되어 반복문이 종료됩니다.  
✅ **(무한 루프 X, 정상적으로 종료됨)**

---

## **📌 추가 설명**
### **무한 루프를 방지하는 방법**
무한 루프를 방지하려면 `break`를 활용하세요!
```python
while True:
    user_input = input("멈추려면 'exit' 입력: ")
    if user_input == "exit":
        break  # 반복문 종료
```

---

### **🔥 결론**
✅ `while True: pass`는 **무한 루프에 빠지는 코드**  
✅ 나머지는 조건이 변하면서 반복이 종료되므로 **무한 루프가 아님**!



## **추가질문**
### **📌 2번 문제 관련: 얕은 복사와 깊은 복사**
> **얕은 복사(Shallow Copy) vs 깊은 복사(Deep Copy)**

---

### **1️⃣ 얕은 복사(Shallow Copy)**
- **기존 객체의 참조(주소)만 복사**하는 방식
- 복사된 객체는 **원본 객체와 같은 메모리 주소를 가리킴**
- **리스트 안에 리스트(중첩 리스트)가 있을 경우, 내부 리스트는 원본과 공유됨**

```python
import copy

# 리스트 생성
original_list = [1, 2, [3, 4]]

# 얕은 복사
shallow_copy = copy.copy(original_list)

# 원본과 복사본 출력 (같은 내용)
print(original_list)  # [1, 2, [3, 4]]
print(shallow_copy)   # [1, 2, [3, 4]]

# 얕은 복사 후, 내부 리스트 수정
shallow_copy[2][0] = 99  # 내부 리스트 값 변경

# 원본 리스트도 영향을 받음!
print(original_list)  # [1, 2, [99, 4]]
print(shallow_copy)   # [1, 2, [99, 4]]
```

🔹 `copy.copy()`를 사용하면 얕은 복사가 이루어지지만, **리스트 안의 리스트(내부 리스트)는 원본과 공유**되므로 내부 요소가 변경되면 원본도 영향을 받습니다.

---

### **2️⃣ 깊은 복사(Deep Copy)**
- **완전히 새로운 객체를 생성**하는 방식
- 원본 객체뿐만 아니라 **내부 리스트까지 완전히 새로운 객체로 복사**
- 원본과 복사본은 완전히 독립적인 메모리 공간을 가짐

```python
import copy

# 리스트 생성
original_list = [1, 2, [3, 4]]

# 깊은 복사
deep_copy = copy.deepcopy(original_list)

# 내부 리스트 수정
deep_copy[2][0] = 99  # 내부 리스트 값 변경

# 원본 리스트는 영향을 받지 않음!
print(original_list)  # [1, 2, [3, 4]]
print(deep_copy)      # [1, 2, [99, 4]]
```

🔹 `copy.deepcopy()`를 사용하면 내부 리스트까지 **완전히 새로운 객체**로 복사되므로, 복사된 리스트를 변경해도 원본에는 영향을 주지 않습니다.

---

### **📌 4번 문제 관련: `return`의 역할과 코드 분석**
#### **1️⃣ `return`을 사용하지 않은 이유**
```python
def modify_list(lst):
    lst.append(4)  # 리스트를 직접 수정

numbers = [1, 2, 3]
modify_list(numbers)
print(numbers)  # [1, 2, 3, 4]
```
✅ 여기서는 **리스트가 가변 객체(mutable object)이기 때문에, 함수 내부에서 리스트를 수정하면 원본도 변경됩니다.**  
✅ 따라서 `return`을 사용하지 않아도, `numbers` 리스트가 직접 변경됩니다.

#### **2️⃣ `return`의 역할**
- `return`은 **함수의 실행 결과를 반환**하는 역할을 합니다.
- 만약 **리스트를 변경하지 않고 새로운 리스트를 반환하고 싶다면**, `return`을 사용해야 합니다.

```python
def modify_list(lst):
    new_lst = lst[:]  # 리스트 복사 (새로운 리스트 생성)
    new_lst.append(4)
    return new_lst
```
✅ **이제 코드 한 줄씩 분석해볼게요!**
```python
numbers = [1, 2, 3]  # 원본 리스트 생성
```
- `numbers`는 `[1, 2, 3]`을 가리키는 리스트입니다.

```python
new_numbers = modify_list(numbers)
```
- `modify_list(numbers)`를 호출하면 `numbers`의 사본(`new_lst`)이 생성되고, `4`가 추가된 새로운 리스트를 반환합니다.

```python
print(numbers)  # [1, 2, 3]
print(new_numbers)  # [1, 2, 3, 4]
```
- ✅ 원본 리스트 `numbers`는 변경되지 않고, `new_numbers`는 새로운 리스트 `[1, 2, 3, 4]`을 가집니다.

🔹 이렇게 하면 **함수 내에서 원본을 변경하지 않고 새로운 리스트를 만들어 반환할 수 있습니다.** (`return`의 역할)

---

### **📌 5번 문제 관련: `while True:`의 의미와 4번 보기 코드 분석**
#### **1️⃣ `while True:`가 항상 참(True)인 이유**
```python
while True:
    pass
```
✅ **`True`는 항상 참(`True`)로 평가되기 때문에, `while True:`는 무조건 실행됩니다.**  
✅ 따라서 `break`가 없으면 프로그램이 **무한 루프**에 빠집니다.

#### **🔹 파이썬에서 항상 참(`True`)으로 평가되는 대표적인 표현**
| 표현 | 평가 결과 |
|------|---------|
| `True` | `True` ✅ |
| `1`, `100`, `-10` (0이 아닌 정수) | `True` ✅ |
| `"hello"`, `" "` (빈 문자열 제외) | `True` ✅ |
| `[1, 2, 3]`, `{}` (빈 리스트 제외) | `True` ✅ |
| `bool(1)`, `bool("text")` | `True` ✅ |

#### **🔹 파이썬에서 항상 거짓(`False`)으로 평가되는 대표적인 표현**
| 표현 | 평가 결과 |
|------|---------|
| `False` | `False` ❌ |
| `0` | `False` ❌ |
| `""` (빈 문자열) | `False` ❌ |
| `[]` (빈 리스트), `{}` (빈 딕셔너리) | `False` ❌ |
| `None` | `False` ❌ |

🔹 따라서 `while True:`는 항상 실행되며, **`break` 문이 없으면 무한 루프**가 됩니다.

---

#### **2️⃣ `while n != 0:` 코드 분석**
```python
n = 5
while n != 0:
    n -= 1
    print(n)
```
✅ **이 코드가 무엇을 위한 코드인지 분석해볼게요!**

1️⃣ `n = 5` → `n`을 5로 초기화합니다.  
2️⃣ `while n != 0:` → `n`이 0이 아니면 반복합니다.  
3️⃣ `n -= 1` → `n`을 1씩 감소시킵니다.  
4️⃣ `print(n)` → 현재 `n`을 출력합니다.

🔹 실행 과정:
```
n = 5  →  출력: 4
n = 4  →  출력: 3
n = 3  →  출력: 2
n = 2  →  출력: 1
n = 1  →  출력: 0
n = 0  →  반복 종료
```
📌 **즉, `n != 0` 조건이 `False`가 되면 `while` 루프가 종료됩니다.**

---

### **📌 최종 정리**
✅ **얕은 복사(Shallow Copy)**: 원본과 내부 리스트를 공유 (변경 시 원본 영향 O)  
✅ **깊은 복사(Deep Copy)**: 완전히 새로운 객체 생성 (변경 시 원본 영향 X)  
✅ **`return`의 역할**: 함수 실행 결과를 반환 (리스트 변경 없이 새로운 리스트 반환 가능)  
✅ **`while True:`**: 항상 실행되며 `break`가 없으면 무한 루프  
✅ **`while n != 0:`**: `n`이 0이 될 때까지 감소하며 반복 실행됨  

