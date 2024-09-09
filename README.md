# AMAMP
This repo provides the source code of our paper: "AMAMP: A Two-Phase Adaptive Multi-hop Attention Message Passing Mechanism For Logical Reasoning Machine Reading Comprehension"

## Citation
If our paper is helpful for your research, please cite this paper in your publications.
```bib
@InProceedings{10.1007/978-3-031-70816-9_18,
author="Phan, Khai T.
and Le, Tung
and Tran, Nhi Thao",
editor="Nguyen, Ngoc Thanh
and Franczyk, Bogdan
and Ludwig, Andr{\'e}
and N{\'u}{\~{n}}ez, Manuel
and Treur, Jan
and Vossen, Gottfried
and Kozierkiewicz, Adrianna",
title="AMAMP: A Two-Phase Adaptive Multi-hop Attention Message Passing Mechanism for Logical Reasoning Machine Reading Comprehension",
booktitle="Computational Collective Intelligence",
year="2024",
publisher="Springer Nature Switzerland",
address="Cham",
pages="224--237",
abstract="Current machine reading comprehension datasets that involve logical reasoning have gained significance in Natural Language Processing. The challenge with these datasets lies in requiring models to comprehend and effectively reason through logical questions, where logical sentences are distantly positioned and lack direct connections. To tackle this challenge, we employ graph diffusion and adaptive mechanisms, aiming to enhance the extraction of information among distant nodes while efficiently mitigating noise during edge expansion and inter-node information propagation. Leveraging advanced Graph Neural Networks, our models - MAMP, LoFiMAMP, and AMAMP - demonstrate effective inference for logical questions by facilitating information exchange among long-distance nodes. Experimental results on the ReClor and LogiQA datasets demonstrate high accuracy, 53.1{\%} and 34.6{\%}, that surpasses all baseline models.",
isbn="978-3-031-70816-9"
}

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
