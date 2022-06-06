# GNNProject_SHAP

Everything lies inside CompGCN+ATT folder.
The zip of datasets are also inside the folder.

Requirements:
torch
dgl-cu102 (depends on cuda version)

To run the training for CompGCN + ATT on full graph run: (Can change the data)
```
python main_hgt_base.py --score_func conve --opn ccorr --gpu 0  --data FB15k-237 --num_bases 50 —optim AdamW
```


To run the training for incomplete graph run

```
python main_ablation.py --score_func conve --opn ccorr  --num_bases 5 --optim AdamW --initial_edge_percentage 0.8  --run_name ablation_80p_hgt_conve_corr_base --gpu  6 —data wn18rr

```

To run the training For Structural Graph Learning run

```
python main_khop.py --score_func conve --opn ccorr --gpu 0  --num_bases 5 --run_name temp --data wn18rr
```
