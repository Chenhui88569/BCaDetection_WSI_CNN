## ECSE484_project_WSIClassification_CNN
### The projdect workflow 
<img src="https://tva1.sinaimg.cn/large/0081Kckwly1glb1stt8x7j31970u0gmu.jpg" alt="ECSE 484_project_work flow" style="5%" />

Three different models are generated 
1. 4Conv_2FC + CWUR-HUP-TCGA cohort(Dataset1)
2. 4Conv_2FC + CWUR-HUP-TCGA-CINJ cohort(Dataset2)
### CNN model configuation 
Two model architectures are used
1. 4Conv_2FC<br>
<img src="https://tva1.sinaimg.cn/large/0081Kckwly1glb2o6s2acj33cu0sigsl.jpg" alt="CNN_diagram_4conv_2FC" />

2. 3Conv_2FC<br>
<img src="https://tva1.sinaimg.cn/large/0081Kckwly1glbm3kv7nhj33cw0u0dv5.jpg" alt="CNN_3conv_diagram" />

### Dataset constitution
Two different datasets are used
1. CWUR-HUP-TCGA cohort(Dataset1)
 CWUR-HUP-TCGA files used in training and validation set. CINJ used in test set
 |                     | CWRU | HUP  | TCGA | CINJ |
   | ------------------- | ---- | ---- | ---- | ---- |
   | Training:positive   | 3000 | 2000 | 2000 | 0    |
   | Training:negative   | 3000 | 2000 | 2000 | 0    |
   | Training: total     | 6000 | 4000 | 4000 | 0    |
   | Validation:positive | 500  | 500  | 500  | 0    |
   | Validation:negative | 500  | 500  | 500  | 0    |
   | Validation: total   | 1000 | 1000 | 1000 | 0    |
   | Testing:positive    | 0    | 0    | 0    | 1500 |
   | Testing:negative    | 0    | 0    | 0    | 1500 |
   | Testing:total       | 0    | 0    | 0    | 3000 |
 
 

2. CWUR-HUP-TCGA-CINJ cohort(Dataset2)
 CWUR-HUP-TCGA-CINJ files used in training and validation set. CINJ used in test set
      |                     | CWRU | HUP  | TCGA | CINJ |
   | ------------------- | ---- | ---- | ---- | ---- |
   | Training:positive   | 1750 | 1750 | 1750 | 1750 |
   | Training:negative   | 1750 | 1750 | 1750 | 1750 |
   | Total training      | 3500 | 3500 | 3500 | 3500 |
   | Validation:positive | 375  | 375  | 375  | 375  |
   | Validation:negative | 375  | 375  | 375  | 375  |
   | Validation:total    | 750  | 750  | 750  | 750  |
   | Testing:positive    | 0    | 0    | 0    | 1500 |
   | Testing:negative    | 0    | 0    | 0    | 1500 |
   | Testing: total      | 0    | 0    | 0    | 3000 |


