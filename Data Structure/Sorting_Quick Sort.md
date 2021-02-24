# Sorting : Quick Sort

> pivot이라는 수를 기준으로 분할하고 정렬한다.



### :closed_book: 개념

퀵 정렬은 `pivot`이라는 임의의 위치에 있는 수를 기준으로 두 개의 리스트로 나눈다. 여기서는 `pivot`을 중앙에 있는 수라고 해보자. 

예를 들어 `[9, 3, 1, 8, 2, 4, 7, 5, 6]`라는 리스트가 존재한다고 해보자. 중앙에 있는 숫자 2를 기준으로 작은 수는 왼쪽에 큰 수는 오른쪽으로 정렬해본다. 그렇다면 `[1]`이 왼쪽에 나머지는 오른쪽으로 리스트에 포함된다. 

이제 나눠진 두 개의 리스트를 재귀호출로 다시 분할하면서 정렬을 해나가면 리스트의 길이가 1이 되었을 때 반환하게 되고 반환이되면서 정렬이 된다.

병합정렬은 분할 후에 정렬을 시키지만 퀵 정렬은 분할하면서 정렬을 한다.



### :bulb: 구현

- 위의 개념을 `python`으로 구현해보자.

- 먼저 리스트의 길이가 1일 때 반환한다.
- 그리고 입력받은 리스트의 중앙값으로 `pivot`을 설정한다.
- 이후 리스트를 탐색하면서 `pivot`보다 작은 수는 왼쪽 리스트, 큰 수는 오른쪽 리스트에 추가한다.
- 그리고 pivot을 포함한 두 개의 리스트를 재귀호출로 다시 나누고 정렬하도록한다.
- 그렇다면 최종적으로 정렬된 리스트가 반환될 것이다.

```python
def quick_sort(numbers):
    if len(numbers) <= 1:
        return numbers
    # 중앙값으로 pivot 설정
    pivot = numbers[len(numbers)//2]
    # pivot을 기준으로 나눌 리스트들
    less_number, number, greater_number = [], [], []
    for idx in range(len(numbers)):
        if numbers[idx] < pivot:
            less_number.append(numbers[idx])
        elif numbers[idx] > pivot:
            greater_number.append(numbers[idx])
        else:
            number.append(numbers[idx])
    return quick_sort(less_number) + number + quick_sort(greater_number)
```



### :hourglass_flowing_sand: 성능

- 퀵 정렬의 시간 복잡도는 **`Big-O 표기법으로 O(nlogn)`**을 갖는다.