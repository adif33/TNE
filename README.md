## our model
<img src="https://github.com/adif33/TNE/blob/main/Architecture.png" width="400" height="400">

The text tokens are first encoded by a SpanBERT MLM encoder. The encoded token representations are used to form a fixed length representation for the span of every NP. The span representations are encoded once more with a Transformer encoder, concatenated to the original encodings and fed to two MLPs to produce an \emph{anchor} and \emph{complement} representation for each NP. The representations are concatenated and fed to a Prediction head


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



