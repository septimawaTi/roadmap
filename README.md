# controller-cards

`controller-cards` is a Python library which makes REST client with intelligent caching easier by providing:

* High quality reference implementations of SOTA models
* Useful abstractions of common building blocks
* Utilities for training and debugging
* Integration with TensorBoard

## Installation

To install `controller-cards`, clone and install requirements:

```
git clone https://github.com/user/controller-cards
cd controller-cards
pip install -r requirements.txt
```

Run tests:

```
python -m unittest discover
```

## Reproducing Results

All models implement a `reproduce` function:

```
python train.py --model data --logdir /tmp/run --use-cuda
```

View metrics:

```
tensorboard --logdir /tmp/run
```

## Example - dashboard

```python
from controller-cards import models

model = models.dashboard(in_channels=1, out_channels=1)
model(batch)
```

## Supported Algorithms

| Algorithm | Score (nats) | Links |
| --- | --- | --- |
| data | **78.61** | [Code](#), [Paper](#) |
| dashboard | 79.17 | [Code](#), [Paper](#) |

## Contributing

Contributions welcome!

