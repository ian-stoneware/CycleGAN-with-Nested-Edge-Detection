# CycleGAN with Nested Edge Detection
 
## Description:
This project contains a CycleGAN model and a CycleGAN+HED model used for chinese painting and real-world landscape image style transfer. And also a CNN model used for comparison with CycleGAN. 

## Installation:
1. Download the dataset from google drive
   ```bash
   https://drive.google.com/file/d/1rSNMLdYqi9pLS5ITbHrjYdhOXM0JXkBk/view?usp=sharing
 <img src="https://github.com/ian-stoneware/CycleGAN-with-Nested-Edge-Detection/blob/main/results/1.png" width="800"/>

2. Follow the steps below to set up the project environment.

- Install [PyTorch](http://pytorch.org) and 0.4+ and other dependencies (e.g., torchvision, [visdom](https://github.com/facebookresearch/visdom) and [dominate](https://github.com/Knio/dominate)).
  - For pip users, please type the command `pip install -r requirements.txt`.
  - For Conda users, you can create a new Conda environment using `conda env create -f environment.yml`.
  - For Docker users, we provide the pre-built Docker image and Dockerfile. Please refer to our [Docker](docs/docker.md) page.
  - For Repl users, please click [![Run on Repl.it](https://repl.it/badge/github/junyanz/pytorch-CycleGAN-and-pix2pix)](https://repl.it/github/junyanz/pytorch-CycleGAN-and-pix2pix).

3. Clone the repository:
   ```bash
   git clone https://github.com/ian-stoneware/CycleGAN-with-Nested-Edge-Detection.git
   
   cd CycleGAN-with-Nested-Edge-Detection

 - To view training results and loss plots, run `python -m visdom.server` and click the URL http://localhost:8097.
 - To log training progress and test images to W&B dashboard, set the `--use_wandb` flag with train and test script

4. Train a model:
  ```bash
  python train.py --dataroot ./datasets/chinesepainting --name chinesepainting_cyclegan --model cycle_gan
  ```
 - replace the `--model cycle_gan` to `--model cycle_gan_hed` switch to the CycleGAN+HED model
 - To see more intermediate results, check out `./checkpoints/chinesepainting_cyclegan/web/index.html`.

5. Test the model:
  ```bash
  python test.py --dataroot ./datasets/chinesepainting --name chinesepainting_cyclegan --model cycle_gan
  ```
 - The test results will be saved to a html file here: `./results/chinesepainting_cyclegan/latest_test/index.html`.

## Results:
<img src="https://github.com/ian-stoneware/CycleGAN-with-Nested-Edge-Detection/blob/main/results/3.png" width="800"/>
<img src="https://github.com/ian-stoneware/CycleGAN-with-Nested-Edge-Detection/blob/main/results/2.png" width="800"/>
Comparison of CycleGAN model with CNN model:
<img src="https://github.com/ian-stoneware/CycleGAN-with-Nested-Edge-Detection/blob/main/results/4.png" width="800"/>
Comparison of CycleGAN model with CycleGAN+HED model:
<img src="https://github.com/ian-stoneware/CycleGAN-with-Nested-Edge-Detection/blob/main/results/5.png" width="800"/>
