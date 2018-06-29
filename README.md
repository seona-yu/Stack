# Stack(자료구조, 알고리즘) 

## 의미
**스택(Stack)이란** 자료구조의 **사전적 정의는 '쌓다' '더미'** 이다.

**아래가 막힌 상자의 구조**를 생각하면 된다. 아래는 막혀있고 위로만 물건을 집어 넣기, 빼기가 가능하다. 

이러한 구조 때문에 먼저 들어온 물건은 나중에 나갈 수 있고, 나중에 들어온 물건은 먼저 나갈 수 있게 된다.

## 용도
스택은 많은 곳에서 사용된다.

가장 편리한 예시를 들면, 인터넷 서핑을 하다가 뒤로가고 싶을 때, 뒤로가기 버튼을 사용하는 것이 있다. 

이 때 **'뒤로가기'버튼**이 바로 **스택(Stack)의 구조**로 만들어져 있다.


제일 마지막에 봤던 페이지는 가장 위에 쌓여져 있고,

제일 마지막에 봤던 페이지부터 한 차례식 '뒤로가기'를 실행하기 때문에,

가장 최근에 본 페이지 즉, **가장 위에 쌓인 물건부터 빼기 시작하는 원리**이다.


## 사용법

- **삽입(Push)**
: **물건을 집어 넣는 것.** 스택의 구조상 **맨 마지막 위치(top)에 데이터가 추가** 된다. 

- **삭제(Pop)**
: **물건을 빼는 것.** Push와 반대되는 개념으로 **맨 마지막 위치(top)부터 데이터가 삭제** 된다.

- **읽기(Peek)**
: 마지막위치(top)에 해당하는 데이터를 읽는다.

## 예시 
### 파이썬으로 스택을 직접 구현. [백준 10828번]
```    
i = int(input())
stack = []
for x in range(i):
    n = input().split()
    if n[0] == 'push':
        stack.append(int(n[1]))
    elif n[0] == 'pop':
        try: 
            print(stack.pop())
        except: 
            print(-1)
            continue
    elif n[0] == 'size':
        print (len(stack))
    elif n[0] == 'empty':
        if len(stack) == 0: 
            print(1)
        else: 
            print(0)
    elif n[0] == 'top':
        if len(stack) == 0: 
            print(-1)
            continue
        print(stack[-1])
```


## 특징 및 장점

컴퓨터에서는 **최근에 참조된 자료가 다시 참조될 확률이 높다.(시간지역성의 원리)**

**스택(Stack)** 은 그 시간지역성을 최고로 활용할 수 있는 자료구조이다.

게다가 스택(Stack)은 **데이터더미** 와 같아서, **구현하기 쉽고 간단하다.**

스케줄링이나 자원관리 등의 여러 분야에서 쓰인다.




