# bdk-python
The Python language bindings for the [bitcoindevkit](https://github.com/bitcoindevkit).

See the [package on PyPI](https://pypi.org/project/bdkpython/).  

## Install from PyPI
Install the latest release using
```shell
pip install bdkpython
```

## Run the tests
```shell
pip3 install --requirement requirements.txt
bash ./generate.sh
python3 setup.py --verbose bdist_wheel
pip3 install ./dist/bdkpython-<yourversion>-py3-none-any.whl
python -m unittest --verbose tests/test_bdk.py
```

## Build the package
```shell
# Install dependencies
pip install --requirement requirements.txt

# Generate the bindings first
bash generate.sh

# Build the wheel
python3 setup.py --verbose bdist_wheel
```

## Run tox to build and test locally
```shell
# install dev requirements
pip install --requirement requirements-dev.txt

# build bindings glue code (located at .bdk-python/src/bdkpython/bdk.py)
source ./generate.sh

# build and test
tox -vv
```

## Install locally
```shell
pip install ./dist/bdkpython-<yourversion>-py3-none-any.whl
```
