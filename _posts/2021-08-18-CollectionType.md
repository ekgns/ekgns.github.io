---
title: "콜렉션 타입 "
categories:
  - Swift
tags:
  - Swift 기분문법
---
## 데이터들의 집합 모음

### Array : 데이터 타입의 값을 순서대로 저장
숫자 0 부터 시작 ( Why?: index 로 번호를 세는데 0부터 시작이여서) <br>
키워드 : [ ] (대괄호)
-   사용방법 : 

```
1. let (이름) : Array<Type> = [값들]
2. let (이름) = [값들]

3. var (이름) : Array<Type> = [값들]
4. var (이름) = [값들]
```
-   ex)

``` 
상수 배열
1.  let name : Array<String> =  [["Bean", "Kim", "Jack", "Joker"]]
1-1. let name: [String] = ["Bean", "Kim", "Jack", "Joker"]



변수 배열
2.  var name2 : Array<String>  = ["Bean", "Kim", "Jack", "Joker"]
2-1. var name2 : [String] = ["Bean", "Kim", "Jack", "Joker"]
2-2. var name = [""]  
```

####   추가 방법! <br>
상수 배열은 값을 추가 x  <br> 
변수 배열은 값을 추가 ㅇ

```
1.  let name : Array<String> =  ["Bean", "Kim", "Jack", "Joker"]
1-1. let name = ["Bean", "Kim", "Jack", "Joker"]
print(name)
---
결과 : ["Bean", "Kim", "Jack", "Joker"] 
---
name.append("Luppy")
name.append("Messy")
name.append("Ryon")
name.append("Son")
print(name)
---
결과 : ["Bean", "Kim", "Jack", "Joker", "Luppy", "Messy", "Ryon", "Son"]
차례대로 저장당함 
---

--- insert 키위드를 이용 --- 
let name : Array<String> =  ["Bean", "Kim", "Jack", "Joker"]
name.insert("Rosa", at: 1) // 1번 인덱스에 로사 추가
print(name)
---
결과 : ["Bean", "Rosa", "Kim", "Jack", "Joker"]
index    0       1       2      3        4
---

```
####  일부 삭제 방법 :

```
var name : Array<String> =  ["Bean", "Rosa", "Kim", "Jack", "Joker"]
name.remove(at: 1)
print(name)
---
결과 : ["Bean", "Kim", "Jack", "Joker"]
---
```


###  Dictionary : 순서없이 Key(키)와 Value(값)이 한 쌍으로 저장  
상수는 추가가 되지 않아서 변수로만 선언

 -   사용방법 : 
 
 ```
 1. var nameAndAge: [String: Int] = ["String 값": Int 값, ... ]
 1-1. var nameAndAge = ["String 값": Int 값, ... ]
 
 ```
 -   ex)

 ``` 
 1. var nameAndAge: [String: Int] = ["Bean": 20, "Kim": 19, "Jack": 4, "Joker": 38]
 var nameAndAge = ["Bean": 20, "Kim": 19, "Jack": 4, "Joker": 38]
 print(nameAndAge)
 
 --- 
 결과 : ["Bean": 20, "Jack": 4, "Joker": 38, "Kim": 19]
 ---
 ```
#### 추가방법 :
 
 ```
 1. var nameAndAge: [String: Int] = ["Bean": 20, "Kim": 19, "Jack": 4, "Joker": 38]
 1-1. var nameAndAge = ["Bean": 20, "Kim": 19, "Jack": 4, "Joker": 38]

 nameAndAge["Luppy"] = 18
 nameAndAge["Messy"] = 32
 nameAndAge["Ryon"] = 10
 nameAndAge["Son"] = 30

 print(nameAndAge)

--- 
결과 : ["Messy": 32, "Ryon": 10, "Son": 30, "Jack": 4, "Joker": 38, "Bean": 20, "Luppy": 18, "Kim": 19]

*** 순서 상관없이 추가 됨 ***
---
 ```
####  일부 삭제 방법 :
 
 ```
 var nameAndAge =  ["Messy": 32, "Ryon": 10, "Son": 30, "Jack": 4, "Joker": 38, "Bean": 20, "Luppy": 18, "Kim": 19]
 
 nameAndAge.removeValue(forKey: "Joker")
 
 ---
 결과 : ["Messy": 32, "Son": 30, "Jack": 4, "Kim": 19, "Luppy": 18, "Ryon": 10, "Bean": 20]
 ---

 ```
 
###  Set : 같은 데이터 타입의 값을 순서 없이 저장
데이터 중복을 허락하지 않는 특징이 있음 

-   사용방법 : 

```
var (이름) : set = Set<Type>()  // 축약형 없음


```
-   ex)

``` 
var name: Set = Set<String>()
name.insert("Bean")
name.insert("Rosa")
name.insert("Jack")
name.insert("Bean")
name.insert("Messi")
print(name)
---
결과: ["Rosa", "Messi", "Bean", "Jack"]
*** Bean을 두번 추가하였으나 한번 밖에 저장되지 않음 *** 
---
```

#### 삭제방법:

```
name.remove("Bean")
print(name)
---
결과: ["Rosa", "Jack", "Messi"]
---

```

