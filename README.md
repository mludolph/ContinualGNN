# Streaming Graph Neural Networks via Continual Learning

Code for [Streaming Graph Neural Networks via Continual Learning](https://dl.acm.org/doi/abs/10.1145/3340531.3411963)（CIKM 2020). ContinualGNN is a streaming graph neural network based on continual learning so that the model is trained incrementally and up-to-date node representations can be obtained at each time step.

## Requirements

- python = 3.8.5
- pytorch = 1.7.1
- scikit-learn = 0.23.2

Requirements can be installed using [poetry](https://python-poetry.org/):

```bash
# create virtual environment
python3 -m venv .venv

# install dependencies
poetry install

# activate environment with dependencies
poetry shell
```

## Usages

- ContinualGNN (proposed model) on Cora:

```bash
cd src/
python main_stream.py --data=cora --new_ratio=0.8 --memory_size=250 --ewc_lambda=80.0
```

- OnlineGNN (lower bound) on Cora:

```bash
python main_stream.py --data=cora
```

If using cuda, set `--cuda`.
