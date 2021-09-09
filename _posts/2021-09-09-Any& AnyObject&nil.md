---
title: "Any&AnyObject&nil"
categories:
  - Swift
tags:
  - Swift 기분문법
---
## Any&AnyObject&nil

###  Any &  AnyObject
- 스위프트의 모든 타입을 수용 가능 /  스위프트의 모든 클래스 타입을 지칭하는 프로토콜
But  Any 타입에 넣은 데이터를 내가 원하는 데이터의 타입으로 할당 할 수 는 없다!!!

- ex) 


```
var any: Any = 100
var i: Int = any
이런식으로 사용 불가 함

class amu {}
var amuObject: AnyObject = amu()

```
## nil
- 없다 / 아무것도 없다 / 비어있다 
일상에선 없다는걸 지칭할 때 0이다 라고 지칭을 한다 하지만 코딩에서는 0은 하나의 값이 없다고 말할 수 없다
그래서 값을 없다고 표시를 해줄거나 비어있는 데이터의를 만들때 사용한다.

- ex)


```
let a:Int = 0
let b:String = "" 
위의 두개는 값이 없는 것이 아니라 값이 있는 것

let a:Int? = nil
let b:String? = nil
이렇게 해줘야 값이 없는것 이다.
```

예제에서 nil을 사용했을때 데이터 타입부분에 대한 차이점이 생겼다.
타입 지정을하면서 ?를 써줬는데 ?는 값이 없을 수 도있다라는 의미의 키워드이다.
데이터 타입의 뒤에 이름을 옵셔널이라고 한다. 

