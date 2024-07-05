# AMAMP
This repo provides the source code of our paper: "AMAMP: A Two-Phase Adaptive Multi-hop Attention Message Passing Mechanism For Logical Reasoning Machine Reading Comprehension"

## Citation
If our paper is helpful for your research, please cite this paper in your publications.
```bib
Waiting for bib
```
## Requirements
```
pip install torch==1.8.0+cu101 -f https://download.pytorch.org/whl/torch_stable.html
pip install dgl-cu101==0.6.1
pip install stanza==1.2.3
pip install transformers==4.5.0
pip install networkx
pip install nltk
pip install scikit-learn
pip install pylev
```

## Evaluation
```shell
export MODE=eval_only
bash scripts/AMAMP_Roberta_LogiQA.sh /PATH/TO/LOGIQA/CHECKPOINTS ## LogiQA evaluation
bash scripts/AMAMP_Roberta_ReClor.sh /PATH/TO/RECLOR/CHECKPOINTS ## ReClor
```

## Training
```shell
export MODE=do_train
bash scripts/AMAMP_Roberta_LogiQA.sh /PATH/TO/ROBERTA ## LogiQA training
bash scripts/AMAMP_Roberta_ReClor.sh /PATH/TO/ROBERTA ## ReClor
```

## Acknowledgement
This repo is built upon the following work:
```
AdaLoGN: Adaptive Logic Graph Network for Reasoning-Based Machine Reading Comprehension.Xiao Li, Gong Cheng, Ziheng Chen, Yawei Sun, Yuzhong Qu. ACL 2024.
https://github.com/nju-websoft/AdaLoGN
```
Many thanks to the authors and developers!
