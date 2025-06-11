formatting is definitely somewhat of an art over a science, but one belief I hold fairly strongly is that

```python
def f(
	arg_1: TypeOfArg1,
	arg_2: TypeOfArg2 | None,
	arg_3: list[SubTypeOfArg3],
) -> ReturnType:
	...
```
and
```python
res = f(
	arg_1=arg_1,
	arg_2=arg_2,
	arg_3=arg_3,
)
```
are a lot more readable than

```python
def f(
	arg_1: TypeOfArg1, arg_2: TypeOfArg2 | None, arg_3: list[SubTypeOfArg3]
) -> ReturnType:
	...
```
and
```python
res = f(
	arg_1=arg_1, arg_2=arg_2, arg_3=arg_3
)
```

---

this obviously becomes a bit more case dependent when we're at the point where it doesn't get split to a new line, e.g.
```python
def f(arg_1: TypeOfArg1, arg_2: TypeOfArg2 | None) -> ReturnType:
	...
```
and 
```python
res = f(arg_1, arg_2)
```
at which point I think it often comes down to "how much is going on in a single line?" and splitting things once there start 
to be non-trivial compound statmeents all going on on the same line
