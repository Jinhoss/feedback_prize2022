# Kaggle_feedback_prize

2022-06-10, feedback v1

```
pretrained model: deberta-v3-base
max_len = 512
data : d_type, d_content
scheduler: warmup
lr = 2e-5
epochs = 3
5fold
focal loss
no dropout
bn
=> 0.788
```



feedback v3

```
pretrained model: deberta-v3-base
max_len = 512
data : d_type, d_content, essay
scheduler: cosineAnnealingLR(T_max=500, eta_min=1e-6)
lr = 1e-5
epochs = 3
dropout = 0.2
no-bn
5fold
ce loss
```

