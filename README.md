## ECSE484_project_WSIClassification_CNN
### The project workflow 
<img src="https://tva1.sinaimg.cn/large/0081Kckwly1glcp49txbxj30xd0u0gms.jpg" alt="ECSE 484_project_work flow_new (1)" style="zoom:5%;" />

Three different models are generated 
1. 4Conv_2FC + CWUR-HUP-TCGA cohort(Dataset1) 
2. 4Conv_2FC + CWUR-HUP-TCGA-CINJ cohort(Dataset2) 
3. 3Conv_2FC + CWUR-HUP-TCGA-CINJ cohort(Dataset2)
### CNN model configuation 
Two model architectures are used
1. 4Conv_2FC<br>
<img src="https://tva1.sinaimg.cn/large/0081Kckwly1glb2o6s2acj33cu0sigsl.jpg" alt="CNN_diagram_4conv_2FC" />

2. 3Conv_2FC<br>
<img src="https://tva1.sinaimg.cn/large/0081Kckwly1glbm3kv7nhj33cw0u0dv5.jpg" alt="CNN_3conv_diagram" />

### Dataset constitution
Two different datasets are used
1. CWUR-HUP-TCGA cohort(Dataset1) <br>
 CWUR-HUP-TCGA files used in training and validation set and CINJ used in test set.<br>
 The numbers of image tiles extracted from four institutions are shown in the table
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

2. CWUR-HUP-TCGA-CINJ cohort(Dataset2) <br>
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
   
### Probability map
   The Probability map is obtain by following the following procedure
1. Load model saved in disc
2. Regularly sample a input WSI and execute image preprocessing. The position of each individual tile is tracked
3. Predict the class of tach tile,obtain probablities
4. Reassemble the tiles. Only tissue tiles are given with probalities and the probablities of non-tissue tiles are zero. 
5. Build heatmap


