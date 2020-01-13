## Function_Annotation
> Function annotaions 는 Function의 다양한 부분과 연관되어 있는 임의의 파이썬 수식이다. 이러한 수식은 compile time에 확인되고, runtime에는 life를 가지지 않는다. 파이썬의 annotation에는 어떠한 의미를 두지 않는다, 강제성을 두지 않는다. Third party 라이브러리에 의해 interprete될 때 life를 가진다. 
## Why use?
- Third party library가 있을 때만 쓸 가치가 있다. 
- 파이썬은 함수를 정의할때 dynamic typing을 허용하는데 Annotation을 통해 함수의 type을 정의 해 줄 수 있다.
- 다른 dependency에서 값을 가져올 때 compile에러로 사전에 명시할 수 있음
## Where to use ? (Application)
1. Annotations for simple parameters : The argument name is followed by ‘:’ which is then followed by the expression. Annotation syntax is shown below.
```python
def foobar(a: expression, b: expression = 5):
```
2. Annotations for excess parameters : Excess parameters for e.g. *args and **kwargs, allow arbitrary number of arguments to be passed in a function call. Annotation syntax of such parameters is shown below.
```python
def foobar(*args: expression, *kwargs: expression):
```
3. Annotations for nested parameters : Nested parameters are useful feature of python 2x where a tuple is passed in a function call and automatic unpacking takes place. This feature is removed in python 3x and manual unpacking should be done. Annotation is done after the variable and not after the tuple as shown below.
```python
def foobar((a: expression, b: expression), (c: expression, d: expression)):
```
4. Annotations for return type : Annotating return type is slightly different from annotating function arguments. The ‘->’ is followed by expression which is further followed by ‘:’. Annotation syntax of return type is shown below.
```
def foobar(a: expression)->expression:
```
