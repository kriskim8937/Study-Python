## Functions

#### filter
- 입력(Callable(함수), Iterable())
- iterable의 값들 중 함수에 넣었을 때 True인 값들만 모아서 list로 만듬
#### map
- 입력(Callable(함수), Iterable())
- iterable의 각각의 값에 함수를 적용한 값들의 list로 만듬
#### join
- 입력(Separator(함수), list(String))
- separator을 기준으로 list의 값들을 전부 합친 string을 return
#### lambda
- lambda a:a*5 
- map, filter, join, reduce 등의 입력으로 많이 쓰임
#### reduce
- 입력(Separator(함수), list(String))
- list를 순회하면서 함수를 적용하여 하나의 값을 만듬 
```python
# 1~200사이의 수 중 7의 배수이고 5의 배수가 아닌 수를 출력하시오
print(','.join(list(map(str,filter(lambda x: x%5!= 0 and x%7==0, range(1,201))))))
```
## reference
- https://book.pythontips.com/en/latest/map_filter.html
- https://programmers.co.kr/learn/courses/4008
