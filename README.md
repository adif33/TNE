## Getting Started

Install dependencies
```shell
conda create -n tne python==3.7 anaconda
conda activate tne

pip install -r requirements.txt
```

## Models

We train the models using [allennlp](https://allennlp.org/)

To run our best model, run:

```bash
allennlp train tne/modeling/configs/coupled_large_att.jsonnet \
         --include-package tne \
         -s models/coupled_spanbert_large_att
```



