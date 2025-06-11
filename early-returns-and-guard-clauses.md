If your function has some special behaviour that is not part of the normal flow, or does some validation, early returns and guard clauses are a great idea

instead of 
```python
def func(d: dict[str, int] | None) -> int | None:
    if d is not None:
        # some complicated logic acting on d and returning something
        return ...
    else:
        return None
```

try

```python
def func(d: dict[str, int] | None) -> int | None:
    if d is None:
        return None
    
    # some complicated logic acting on d and returning something
    return ...
```
