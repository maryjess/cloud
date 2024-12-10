# linting
* analysing code for:
  * potential errors
  * formatting issue
  * stylistic inconsistencies
  * suspicious constructs


* helps to:
  * enforce standards
  * avoid mistakes

# virtualisation
* abstracting compute resources from the underlying physical hardware to improve utilisation and flexibility
* allows multiple VMs to run on one server

# requirements.txt
* file listing all Python package dependencies needed for a Project
* allows easily replicating environment and managing versions

```
# requirements.txt

pylint==2.5.0
pytest==7.2.0
```

```
# command to install dependencies

pip install -r requirements.txt 
```

# modularity
* breaking a system into Logical Components with clearly defined inputs / outputs
* allows reuse, testing and updating of individual modules

```
# calculator.py module

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y
```
```
import calculator

x = 5
y = 3

# Calling add function from external module
print(calculator.add(x, y))

# Enables reusing logic in a modular way
```

# idempotence
* ability to apply an operation multiple times without changing the result
* makes workflows more robust to failure by allowing replay without risk

```
def set_flag(flag):
    # Sets flag to True, no matter current value
    flag = True
    print(f"Flag is now {flag}")

flag1 = True
flag2 = False

set_flag(flag1) # Flag is now True
set_flag(flag1) # Flag is now True - Idempotent

set_flag(flag2) # Flag is now True
```