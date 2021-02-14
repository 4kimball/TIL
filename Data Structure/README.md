# Data Structure

> python으로 알아보는 자료구조



## 선형 자료구조

### Stack

스택은 데이터를 한 쪽에서만 넣고 빼는 자료구조이다. 그렇기 때문에 후입선출 `Last In First Out - LIFO`의 특징을 갖고있다. 데이터를 입력하면 계속 쌓이는 구조가되며 가장 마지막에 넣은 데이터가 맨 위에 위치한다.

python에서는 `list`를 활용하여 스택을 구현할 수 있다. 데이터를 넣고 빼는 입구가 하나로 생각하고 맨 뒤로 데이터를 넣고 빼도록한다.

- `.append()` : 스택에 데이터를 넣는다.
- `stack[-1]` : 맨 뒤에 있는 데이터를 가리킨다.
- `.pop()` : 맨 뒤에 있는 데이터를 제거한다.
  - `O(1)`의 시간복잡도를 갖는다.

```python
stack = []
stack.append(1)
stack.append(2)
stack.append(3)
stack.append(4)
print(stack[-1]) # 4 출력

stack.pop() # 맨 뒤에있는 4 제거
print(stack[-1]) # 3 출력
```



### Queue

큐는 뒤로 데이터를 넣고 앞에서 데이터를 빼는 자료구조이다. 그렇기 때문에 선입선출 `First In First Out - FIFO`의 특징을 갖고있다. 데이터를 넣은 순서대로 뺄 수 있다.

python에서 `list`를 활용하여 큐를 구현한다. 데이터를 넣을 때는 뒤에서, 뺄 때는 앞에서 빼도록 한다.

- `.append()` : 큐에 데이터를 넣는다.
- `queue[0]` : 맨 앞에있는 데이터를 가리킨다.
- `queue.pop(0)` : 맨 앞에있는 데이터를 제거한다.
  - `O(n)`의 시간복잡도를 갖는다.

```python
queue = []
queue.append(1)
queue.append(2)
queue.append(3)
queue.append(4)
print(queue[0]) # 1 출력

queue.pop(0) # 1을 제거한다.
print(queue[0]) # 2 출력
```



### Deque

덱은 데이터를 넣고 빼는 작업을 양쪽에서 할 수 있다. 즉 왼쪽에서도 데이터를 넣고 빼고, 오른쪽에서도 데이터를 넣고 뺄 수 있다. 

python에서 `list`로 큐를 구현할 때 앞에있는 데이터를 `pop(0)`으로 제거하는데 이는 `O(n)`의 시간복잡도를 갖고있기 때문에 비효율적이다. 하지만 python의 `deque`의 경우 큐에서 데이터의 제거를 `O(1)`로 할 수 있다.

먼저 `_collections`에서 `deque`를 가져온다. 

- `.popleft()` : 가장 앞에있는 원소를 반환하고 제거한다.
- `appendleft()` : 가장 앞에 원소를 추가한다.
- `.pop()`, `.append()` : `list`에 썼던 함수도 그대로 사용할 수 있다.

```python
from _collections import deque

q = deque() # 빈 덱을 생성한다.
q.append(1)
q.append(2)
q.append(3) # 데이터를 넣을 때는 append를 사용하여 뒤로 넣는다.
print(q.popleft()) # 1이 출력된다.
print(q.popleft()) # 2가 출력된다.
```



