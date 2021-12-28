# fastunit

Async unittest of Python3. Run testcases with coroutine.

## Usage

1. Download/Git clone source code, and run `./install.sh` (or `python setup.py install`) to install.

2. Replace `unittest` with `fastunit` in your code.

_Optional_: Modify the number of test being run in parallel:
```
runner = fastunit.TextTestRunner()
runner.run(suite, nworkers=5)
```
The defaults behaviour [depends on the Python version](https://docs.python.org/3/library/concurrent.futures.html#concurrent.futures.ThreadPoolExecutor).

## Known problem:

`HTMLTestRunner` is not supported, for it designed for linear testcase.
