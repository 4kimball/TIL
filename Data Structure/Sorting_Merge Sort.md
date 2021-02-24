# Sorting : Merge Sort

> 정렬할 수열을 분할하여 가장 작은 단위에 도달했을 때부터 정렬해온다.



### :closed_book: 개념

병합정렬은 두 가지의 과정을 거친다. 정렬을 진행할 리스트를 가장 작은 단위로 분할하는 과정과 분할된 리스트들을 정렬하는 과정을 거친다.

- **리스트 분할하기**

`[9, 3, 1, 8, 2, 4, 7, 5, 6]`이라는 리스트가 있다. 이를 가장 작은 단위로 분할을 하게 되면 `[9]`, `[3]`, `[1]` 처럼 크기가 1인 리스트를 갖게된다. 분할하는 과정을 살펴보면 계속해서 가운데를 기준으로 두 리스트로 만들어 나간다. 이렇게 두 개의 리스트로 나누다보면 마지막엔 1개의 원소만 들어있는 리스트가 생성된다.



- **분할된 리스트 정렬하기**

1개의 원소를 갖는 리스트로 분할했다면 이제 정렬을 해나간다. 위의 예시를 보면 `[9]`와 `[3]`의 크기를 비교하여 작은 수를 리스트에 넣는다. 그러면 이제 `[9]`만 남게되고 `[9]`를 3이 들어있는 리스트에 넣어 합치게된다. 이 과정을 거치면 최종적으로 정렬된 리스트가 반환된다.

이때 3개의 숫자를 갖는 왼쪽  리스트와 오른쪽 리스트가 있을 때 왼쪽 리스트에 작은 숫자가 몰려있어 왼쪽 리스트는 길이가 0이 될 때 오른쪽은 아직 3개의 원소가 남아있다면 뒤에 이어서 첫 번째 숫자부터 넣어준다.



위의 두 가지 과정을 거쳐 분할 후에 정복(정렬)하는 알고리즘을 `분할정복`이라고 한다. 처음 9개의 숫자를 갖는 리스트를 정렬하는 것보다 2개의 원소를 갖는 리스트를 정렬하는 것이 더 쉽기 때문에 가장 작은 단위로 분할 후에 다시 합치는 것이다.



### :bulb: 구현

- 위의 개념을 `python`으로 구현해보자.
- 먼저 리스트를 1개의 숫자를 갖게될 때까지 분할하는 과정이다.
- 기본적으로 재귀호출을 통해 이루어지며 리스트의 길이가 1일 때 반환하게 된다.
- 그리고 입력된 리스트를 중간값을 기준으로 왼쪽과 오른쪽으로 이분한다.
- 이분된 리스트를 재귀호출로 다시 분할하도록 한다.

```python
# 데이터를 분할하는 과정
def merge_sort(numbers):
    if len(numbers) <= 1:
        return numbers
    mid = len(numbers)//2
    left_numbers = numbers[:mid]
    right_numbers = numbers[mid:]
    left_numbers = merge_sort(left_numbers)
    right_numbers = merge_sort(right_numbers)

    # 분할 후에 정복해나가기 (우선순위에 따라 정렬해간다.)
    return merge(left_numbers, right_numbers)
```



- 분할 후에 정렬을 하는 과정이다.
- 분할된 왼쪽 리스트와 오른쪽 리스트가 입력이 되며 최종적으로 `result`라는 리스트에 정렬된 숫자를 넣어 반환한다.
- `while`문을 통해 두 개의 리스트의 길이가 0일 때까지 반복된다.
- 세 가지의 경우에 따라 정렬이 이루어진다.
  - 가장 처음 두 개의 리스트 모두 숫자가 남아있을 때 각 리스트의 첫 번째 원소를 비교한다.
  - 왼쪽 리스트만 남아있다면 왼쪽 리스트의 첫 번째 원소부터 `result`에 추가한다.
  - 오른쪽 리스트만 남아있다면 오른쪽 리스트의 첫 번째 원소부터 `result`에 추가한다.
- 위의 과정을 거친 후에 정렬된 리스트를 반환하도록 한다.

```python
def merge(left_numbers, right_numbers):
    result = []
    # 왼쪽 리스트와 오른쪽 리스트가 모두 빌 때까지 정렬
    while len(left_numbers) > 0 or len(right_numbers):
        # 두 리스트 모두 데이터가 남아있을 때
        if len(left_numbers) > 0 and len(right_numbers) > 0:
            # 왼쪽 리스트의 첫 번째와 오른쪽 리스트의 첫 번째를 비교한다.
            if left_numbers[0] < right_numbers[0]:
                result.append(left_numbers[0])
                left_numbers = left_numbers[1:]
            else:
                result.append(right_numbers[0])
                right_numbers = right_numbers[1:]
        # 왼쪽 리스트만 남아있을 때
        elif len(left_numbers) > 0:
            result.append(left_numbers[0])
            left_numbers = left_numbers[1:]
        # 오른쪽 리스트만 남아있을 때
        elif len(right_numbers) > 0:
            result.append(right_numbers[0])
            right_numbers = right_numbers[1:]

    return result
```



### :hourglass_flowing_sand: 성능

- 병합 정렬의 시간 복잡도는 **`Big-O 표기법으로 O(nlogn)`**을 갖는다.
- 정렬할 숫자가 n개 일 때 각각의 병합 단계마다 최대 n번의 비교연산이 진행된다.