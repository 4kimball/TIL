# Sorting : Selection Sort

> 수열 중에서 최솟값을 선택하여 맨 앞의 숫자와 자리를 바꿔주면서 정렬이된다. 



### :orange_book: 개념

선택 정렬은 쉽고 간단하다. `[5, 2, 4, 3, 1]`이라는 수열이 있을 때 매 탐색마다 최솟값의 인덱스를 찾아서 맨 왼쪽으로 이동시키며 맨 왼쪽에 있는 숫자는 최솟값이 있던 자리로 옮겨준다.

위와 같은 동작을 반복하면 왼쪽부터 정렬이되기 때문에 최솟값을 찾을 인덱스를 하나씩 증가시켜줘야 한다.



### :bulb: 구현

- 위의 개념을 `python`으로 구현해보자.
- 첫 번째 `for`문에서 최솟값을 비교해서 찾을 변수인 `min_idx`에 정렬할 자리의 인덱스를 할당한다.
- 두 번째 `for`문에서는 `i`보다 한 칸 많은 왼쪽부터 최솟값을 탐색하게된다.
- 계속해서 최솟값을 찾아서 해당 인덱스를 `min_idx`에 넣어준다.
- 두 번째 `for`문이 종료되었다면 `i`와 `min_idx`의 인덱스에 있는 값을 교환해준다.

```python
numbers = [5, 2, 4, 3, 1]

for i in range(len(numbers)):
    min_idx = i
    for j in range(i+1, len(numbers)):
        if numbers[min_idx] > numbers[j]:
            min_idx = j

    numbers[i], numbers[min_idx] = numbers[min_idx], numbers[i]

print(numbers)
# [1, 2, 3, 4, 5]
```



### :hourglass_flowing_sand: 성능

- 선택 정렬의 시간 복잡도는 **`Big-O 표기법으로 O(n^2)`** 를 갖는다.
- 두 번째 `for`문은 (n-1), (n-2), (n-3) - - - 번씩 최솟값을 찾기위한 비교연산이 진행된다.
  - 이것은 버블정렬과 같게되며 각각의 비교횟수를 더하면 등차수열의 합이 되고 이는 O(n^2)가 된다.