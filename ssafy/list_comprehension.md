# **📌 리스트 컴프리헨션(List Comprehension) 완벽 정리**
✅ **리스트 컴프리헨션(List Comprehension)**은 **리스트를 만드는 간결한 방법**입니다.  
✅ **기존의 `for`문을 사용한 리스트 생성 코드보다 간결하고 직관적**입니다.  
✅ **하나씩 단계적으로 설명해 드릴 테니 차근차근 이해해 보세요!** 🚀  

---

## **1️⃣ 리스트 컴프리헨션 기본 문법**
✅ **일반적인 리스트 컴프리헨션의 기본 문법**
```python
[표현식 for 변수 in 반복가능한객체]
```
✅ **기본 `for`문과 비교하여 차이를 알아봅시다.**

### **📌 예제 1: 1부터 5까지의 숫자를 리스트에 저장**
✅ **기존 `for`문 사용**
```python
numbers = []
for i in range(1, 6):
    numbers.append(i)

print(numbers)  # [1, 2, 3, 4, 5]
```
✅ **리스트 컴프리헨션 사용**
```python
numbers = [i for i in range(1, 6)]
print(numbers)  # [1, 2, 3, 4, 5]
```
✅ **리스트 컴프리헨션을 사용하면 한 줄로 간결하게 표현할 수 있습니다.**  

---

## **2️⃣ 리스트 컴프리헨션 + 조건문**
✅ **리스트 컴프리헨션에는 `if`문을 추가할 수 있습니다.**  

### **📌 예제 2: 짝수만 저장**
✅ **기존 `for`문 사용**
```python
even_numbers = []
for i in range(1, 11):
    if i % 2 == 0:
        even_numbers.append(i)

print(even_numbers)  # [2, 4, 6, 8, 10]
```
✅ **리스트 컴프리헨션 사용**
```python
even_numbers = [i for i in range(1, 11) if i % 2 == 0]
print(even_numbers)  # [2, 4, 6, 8, 10]
```
✅ **조건을 리스트 컴프리헨션 안에서 바로 추가할 수 있습니다!**  

---

## **3️⃣ 리스트 컴프리헨션 + `if-else`**
✅ **`if-else` 문을 포함하는 리스트 컴프리헨션**
```python
[표현식 if 조건 else 다른표현식 for 변수 in 반복가능한객체]
```

### **📌 예제 3: 홀수는 "odd", 짝수는 "even" 저장**
✅ **기존 `for`문 사용**
```python
numbers = []
for i in range(1, 6):
    if i % 2 == 0:
        numbers.append("even")
    else:
        numbers.append("odd")

print(numbers)  # ['odd', 'even', 'odd', 'even', 'odd']
```
✅ **리스트 컴프리헨션 사용**
```python
numbers = ["even" if i % 2 == 0 else "odd" for i in range(1, 6)]
print(numbers)  # ['odd', 'even', 'odd', 'even', 'odd']
```
✅ **`if-else`를 리스트 컴프리헨션 내부에서 사용할 수 있습니다.**  

---

## **4️⃣ 리스트 컴프리헨션 + 중첩 반복문**
✅ **이중 `for`문을 포함하는 리스트 컴프리헨션**
```python
[표현식 for 변수1 in 반복가능한객체1 for 변수2 in 반복가능한객체2]
```

### **📌 예제 4: 두 리스트의 곱 저장**
✅ **기존 `for`문 사용**
```python
result = []
for x in [1, 2, 3]:
    for y in [4, 5, 6]:
        result.append(x * y)

print(result)  # [4, 5, 6, 8, 10, 12, 12, 15, 18]
```
✅ **리스트 컴프리헨션 사용**
```python
result = [x * y for x in [1, 2, 3] for y in [4, 5, 6]]
print(result)  # [4, 5, 6, 8, 10, 12, 12, 15, 18]
```
✅ **중첩 `for`문을 한 줄로 표현할 수 있습니다!**  

---

## **5️⃣ 리스트 컴프리헨션을 `for`문으로 변환하는 연습**
✅ **리스트 컴프리헨션이 헷갈릴 때는 `for`문으로 변환하면 이해하기 쉽습니다.**  

✅ **리스트 컴프리헨션**
```python
squares = [x ** 2 for x in range(1, 6)]
```
✅ **같은 코드의 `for`문 버전**
```python
squares = []
for x in range(1, 6):
    squares.append(x ** 2)
```
✅ **이제 리스트 컴프리헨션을 읽을 때 `for`문으로 변환하는 연습을 해보세요!**  

---

## **📌 최종 정리**
| 유형 | 예제 코드 | 결과 |
|------|---------|------|
| 기본 리스트 컴프리헨션 | `[i for i in range(1, 6)]` | `[1, 2, 3, 4, 5]` |
| `if` 포함 | `[i for i in range(1, 11) if i % 2 == 0]` | `[2, 4, 6, 8, 10]` |
| `if-else` 포함 | `["even" if i % 2 == 0 else "odd" for i in range(1, 6)]` | `['odd', 'even', 'odd', 'even', 'odd']` |
| 중첩 `for`문 | `[x * y for x in [1, 2, 3] for y in [4, 5, 6]]` | `[4, 5, 6, 8, 10, 12, 12, 15, 18]` |

---

📌 **이제 리스트 컴프리헨션이 확실히 이해되셨나요? 😊**  
📌 **추가 질문이 있으면 언제든지 물어보세요! 🚀**
