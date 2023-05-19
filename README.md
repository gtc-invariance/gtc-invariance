# The $G$-Triple Correlation Layer for Robust $G$-Invariance in $G$-Equivariant Networks

This repository is the official accompaniment to _A General Framework for Robust G-Invariance in G-Equivariant Networks_ (submitted, NeurIPS 2023)

## Installation

To install the requirements and package, run:

```
pip install -r requirements.txt
python install -e .
```

## Datasets

To download the datasets, run:

```
wget --load-cookies /tmp/cookies.txt "https://docs.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies /tmp/cookies.txt --keep-session-cookies --no-check-certificate '[URL]' -O- | sed -rn 's/.*confirm=([0-9A-Za-z_]+).*/\1\n/p')&id=[ID]" -O datasets.zip 
rm -rf /tmp/cookies.txt
unzip datasets.zip
rm -r datasets.zip
```


If your machine doesn't have wget, follow these steps: 
1. Download the zip file [here]([URL]).
2. Place the file in the top node of this directory, i.e. in `tc-invariance/`.
3. Run:
    ```
    unzip datasets.zip
    rm -r datasets.zip
    ```

## Training

To train the models in the paper, run the following commands.

```
python train.py --config rotation_experiment
python train.py --config translation_experiment
```

To run on GPU, add the following argument, with the integer specifying the device number, i.e.:


```
--device 0
```

The full set of hyperparameters and training configurations are specified in the config files in the ```configs/``` folder.

To view learning curves in Tensorboard, run:
```
tensorboard --logdir logs/
```

## Pre-trained Models

The pre-trained models are included in the repo, in the following locations:

```
logs/gtc/
logs/max/
```


## Results and Figures

All results and figures from the paper are generated in the Jupyter notebooks located at:

```
notebooks/file.ipynb
```

## License

This repository is licensed under the MIT License.  
