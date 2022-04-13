## our model
<img src="https://https://github.com/adif33/TNE/blob/main/Architecture.png" width="100" height="100">



## Getting Started

Install dependencies
```shell
conda create -n tne python==3.7 anaconda
conda activate tne

pip install -r requirements.txt
```

## train
To train our best model, run:

```bash
allennlp train tne/modeling/configs/coupled_large_att.jsonnet \
         --include-package tne \
         -s models/coupled_spanbert_large_att
```



