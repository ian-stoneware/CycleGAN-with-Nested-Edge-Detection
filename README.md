# CycleGAN with Nested Edge Detection
 
## Description:
This project contains a CycleGAN model and a CycleGAN+HED model used for chinese painting and real-world landscape image style transfer. And also a CNN model used for comparison with CycleGAN. 

## Installation:
1. Download the dataset from google drive
   ```bash
   https://drive.google.com/file/d/1rSNMLdYqi9pLS5ITbHrjYdhOXM0JXkBk/view?usp=sharing
2. Clone the repository:
   ```bash
   git clone https://github.com/ian-stoneware/CycleGAN-with-Nested-Edge-Detection.git
   
   cd CycleGAN-with-Nested-Edge-Detection
To view training results and loss plots, run python -m visdom.server and click the URL http://localhost:8097.
To log training progress and test images to W&B dashboard, set the --use_wandb flag with train and test script

3. Train a model:
  ```bash
  python train.py --dataroot ./datasets/maps --name maps_cyclegan --model cycle_gan
