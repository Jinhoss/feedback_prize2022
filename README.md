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

```
model2 saved
1   Average valid loss: 0.7294
  Accuracy: 0.6772
100%|██████████| 3676/3676 [41:26<00:00,  1.48it/s, Epoch=1, LR=2.81e-6, Train_Loss=0.63] 
100%|██████████| 459/459 [03:19<00:00,  2.31it/s, Epoch=1, LR=2.81e-6, Train_Loss=0.746]
2   Average valid loss: 0.7460
  Accuracy: 0.6740
100%|██████████| 3676/3676 [41:25<00:00,  1.48it/s, Epoch=2, LR=9.93e-6, Train_Loss=0.553]
100%|██████████| 459/459 [03:18<00:00,  2.31it/s, Epoch=2, LR=9.93e-6, Train_Loss=0.734]
early stop 2 fold, 2 epcoh_i
3   Average valid loss: 0.7344
  Accuracy: 0.6859
Some weights of the model checkpoint at microsoft/deberta-v3-base were not used when initializing DebertaV2Model: ['mask_predictions.classifier.bias', 'mask_predictions.classifier.weight', 'mask_predictions.LayerNorm.bias', 'mask_predictions.LayerNorm.weight', 'lm_predictions.lm_head.LayerNorm.weight', 'lm_predictions.lm_head.dense.bias', 'mask_predictions.dense.weight', 'lm_predictions.lm_head.LayerNorm.bias', 'lm_predictions.lm_head.bias', 'mask_predictions.dense.bias', 'lm_predictions.lm_head.dense.weight']
- This IS expected if you are initializing DebertaV2Model from the checkpoint of a model trained on another task or with another architecture (e.g. initializing a BertForSequenceClassification model from a BertForPreTraining model).
- This IS NOT expected if you are initializing DebertaV2Model from the checkpoint of a model that you expect to be exactly identical (initializing a BertForSequenceClassification model from a BertForSequenceClassification model).
------------fold no---------3----------------------
100%|██████████| 3676/3676 [41:23<00:00,  1.48it/s, Epoch=0, LR=3.48e-6, Train_Loss=0.727]
100%|██████████| 459/459 [03:18<00:00,  2.31it/s, Epoch=0, LR=3.48e-6, Train_Loss=0.709]
model3 saved
1   Average valid loss: 0.7090
  Accuracy: 0.6929
100%|██████████| 3676/3676 [41:26<00:00,  1.48it/s, Epoch=1, LR=2.81e-6, Train_Loss=0.63] 
100%|██████████| 459/459 [03:18<00:00,  2.31it/s, Epoch=1, LR=2.81e-6, Train_Loss=0.712]
2   Average valid loss: 0.7117
  Accuracy: 0.6946
100%|██████████| 3676/3676 [41:24<00:00,  1.48it/s, Epoch=2, LR=9.93e-6, Train_Loss=0.556]
100%|██████████| 459/459 [03:18<00:00,  2.31it/s, Epoch=2, LR=9.93e-6, Train_Loss=0.703]
model3 saved
3   Average valid loss: 0.7032
  Accuracy: 0.7141
```



feedback v4

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
focal loss
```



feedback v4 focal loss, no bn

```
model1 saved
1   Average valid loss: 0.7200
  Accuracy: 0.6770
100%|██████████| 3676/3676 [41:25<00:00,  1.48it/s, Epoch=1, LR=2.81e-6, Train_Loss=0.232]
100%|██████████| 459/459 [03:18<00:00,  2.31it/s, Epoch=1, LR=2.81e-6, Valid_Loss=0.715]
model1 saved
2   Average valid loss: 0.7146
  Accuracy: 0.6750
100%|██████████| 3676/3676 [41:24<00:00,  1.48it/s, Epoch=2, LR=9.93e-6, Train_Loss=0.196]
100%|██████████| 459/459 [03:17<00:00,  2.32it/s, Epoch=2, LR=9.93e-6, Valid_Loss=0.69] 
model1 saved
3   Average valid loss: 0.6899
  Accuracy: 0.6936
```

