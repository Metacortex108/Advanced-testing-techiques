# Advanced-testing-techiques
This is to test the advanced testing techniques

# Setup
1. Create and source virtualenv

```bash
virtual env: virtualenv ~/.advanced-testing
source ~/.advanced-testing/bin/activate
```

2. Create a scaffold project
```bash
 touch MakeFile
 touch hello.py
 touch test_hello.py
 touch requirements.txt
``` 

3. Populate 'Makefile'

```bash
install:
	pip install --upgrade pip &&\
		pip install -r requirements.txt
test:
    python -m pytest -vv --cov=hello --cov=hellocli test_hello.py
lint:
	pylint --disable=R,C hello.py hellocli.py

all: install lint test
```

###How to debug

* Print
* Print debugging
* testing