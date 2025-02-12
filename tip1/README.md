# Add '`__main__`' for the program
Every time import module – it imports the whole script. 

Always check if `__name__ == '__main__'` and insert functionality. This construction will ensure that it runs only if module is launched directly. 
Also it works at some point as self documentation, as it shows where the program is launching. 

## Code Example
### `module.py`
```python
import time  
  
  
def connect() -> None:  
    print('Connecting...')  
    time.sleep(3)  
    print('You are connected!')  
  
  
if __name__ == '__main__':  
    connect()
```
### `main.py`
```python
from module import connect  
  
if __name__ == '__main__':  
    connect()
```