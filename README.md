<div align="center">

# 360 Video Category Agnostic Counting

<font size="4">
YEN-LUN CHOU&emsp;
</font>
<br>

<font size="4">
National Chung Chi University
</font>

| <a href="https://github.com/Allenchou0708/360-Video-Category-Agnostic-Counting/blob/main/360%20Video%20CAC%20%E6%8A%95%E5%BD%B1%E7%89%87.pdf">Project Description Slide</a> |


![360_video_cac_cover_image](https://github.com/user-attachments/assets/1f12bd90-8771-447f-81d9-ad6a90d7a791)

</div>

<br>
<br>


## Abstract

In the task of object counting for 360° videos, previous studies have relied on reprojecting each equirectangular frame (ERP) into multiple perspective views, which significantly slows down the inference process. To eliminate this time-consuming reprojection step, we propose to perform object counting directly on ERP images. By revising the CFOCNet architecture and introducing a deform feature to better handle distortions inherent in ERP images, our method achieves competitive performance in terms of Normalized Absolute Error (NAE) and Squared Relative Error (SRE), while substantially improving computational efficiency.

<br>
<br>

## Installation
1. Download the notebook<br>
   Download [360-video-class-agnostic-couting.ipynb](https://github.com/Allenchou0708/360-Video-Category-Agnostic-Counting/blob/main/360-video-class-agnostic-couting.ipynb) from this repository and upload it to your Kaggle workspace.

2. Prepare the dataset<br>
   Import the [dataset](#datasets) into your Kaggle notebook environment.

3. Run the experiments<br>
   All dependencies listed in requirements.txt are already pre-installed within the provided notebook. You can now directly execute the notebook cells to reproduce the experiments.

<br>
<br>

## Metrics

<div align="center">

$$
\text{Normalized Absolute Error, NAE} = \frac{1}{L} \sum_{l=1}^{L} \frac{| \tilde{c}_l - c_l |}{c_l}
$$

$$
\text{Squared Relative Error, SRE} = \sqrt{ \frac{1}{L} \sum_{l=1}^{L} \frac{(\tilde{c}_l - c_l)^2}{c_l} }
$$


</div>

<br>
<br>

## Datasets

We use the [360 Dataset + Pandora Dataset](https://www.kaggle.com/datasets/allenchou78/pandora-clean-straight-dataset-correct/data)
 in our experiments

<br>
<br>

## Performance 

| Model | NAE | SRE | Inference Time (FPS) | 
| :-- | :-: | :-: | :-: |
| **360 Video CAC - B** | **0.386** | **4.835** | **24.42** |
| **360 Video CAC - DF** | **0.356** | **3.909** | **21.39** |

<br>
<br>
