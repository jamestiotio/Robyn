# Robyn

Robyn is an async Python backend server with a runtime written in Rust, btw.

Python server running on top of of Rust Async RunTime.

## Installation

You can simply use Pip for installation.

```
pip install robyn
```

## Usage

```python

from robyn import Robyn

app = Robyn()

@app.get("/")
async def h():
    return "Hello, world!"

app.start()

```

## Contributor Guidelines

Feel free to open an issue for any clarification or for any suggestions.

To read about the detailed architecture, you can read [here](https://raw.githubusercontent.com/sansyrox/robyn/main/docs/architecture.md).

## Testing on Python

1. `cargo build --release`
2. `cp target/release/librobyn.dylib ./robyn.so`
3. `python3`
4. `import robyn`
5. `dir(robyn)`

## To Run

1. Add more routes in the test.py file(if you like). It only supports only get requests at the moment

2. Run `maturin develop`

3. Run `python3 test.py`

4. To measure the performance: `./server_test.sh`