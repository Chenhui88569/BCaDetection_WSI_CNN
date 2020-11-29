# ECSE484_project_WSIClassification_CNN
## Tile-structured dataset formation and Image prepossessing--Workflow
1. dataset rearrangement,combination of images from different cohorts to establish training set. As to validation and test dataset, the images from the specfic cohort are randomly selected.  
2. tile regular sampling
3. labeling
4. color space transformation
5. Standardization and then normalization. Specifically, pixel values are standardized to the range [-1,1] and then rescaled the values from [-1,1] to [0,1].
6. image augmentation.If noninvasive breast cancer is the dominant class among the tiled samples, image augmentation is used to enlarge postive sets mandatorily so that balanced dataset is guaranteed. undersampling and oversampling.
