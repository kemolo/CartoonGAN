# CartoonGAN
# update 2020.02.24:
# Our paper "Learning to Cartoonize Using White-Box Cartoon Representations" is accepted to CVPR2020. Relevent repository, code and pre-trained model will be made publicly available later.

The repo for our paper is https://github.com/SystemErrorWang/White-box-Cartoonization, now inference code and pre-trained data is available, other information will be updated later

update 2019.08.08
upload a new script and npy weight, now you can cartoonize image with random size.

update 2019.07.18
Upload some results of my new model. It's much better than before. 
A pre-trained model is also available now, please feel free to try your own data.
The training settings are quite different from the original pape now. Maybe i will write a paper about it

update 2019.09.16
Added some result of my new model, writing papers now. 

demo video is available on bilibili:
https://www.bilibili.com/video/av56708333#reply1789899604

some new results:

![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/WechatIMG76.jpeg?raw=true)
![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/WechatIMG77.jpeg?raw=true)
![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/WechatIMG78.jpeg?raw=true)
![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/WechatIMG79.jpeg?raw=true)
![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/cartoon_gakki1.jpg)
![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/cartoon_gakki2.jpg)
![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/cartoon_scenery2.jpg)
![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/cartoon_shanghai.jpg)
![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/cartoon_tower1.jpg)

update 2019.06.18:
I designed a new model, trained it with new dataset and got much better cartoonization quality
Still, you can find old scripts in 'old_code' folder, and run training script with description below.


![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/7499_train.png)
![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/7999_train.png)
![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/8499_train.png)

This is a tensorflow implementation of Cartoon GAN published in CVPR2018 (http://openaccess.thecvf.com/content_cvpr_2018/papers/Chen_CartoonGAN_Generative_Adversarial_CVPR_2018_paper.pdf). The network is loosely based on the paper but has a few changes: input size is 96(256 in original paper), patch size for discriminator is 28(70 in original paper), less channels and stacked residual blocks for generator and discriminator network, different hyperparameters.

In this implementation, we use celeba dataset for real person images and getchu dataset (https://github.com/shaform/GirlsManifold) for cartoon style images. All images were center cropped into square shape and then resized to 96. For the edge-blured images, I simply applied gaussian blur with kernel size 5 for convenience. You also need to download a pre-trained vgg19 model and locate in in the save folder. (https://mega.nz/#!xZ8glS6J!MAnE91ND_WyfZ_8mvkuSa2YcA7q-1ehfSm-Q1fxOvvs)

This code is based on Tensorflow 1.8, Python 3.6, and was tested in both windows10 and ubuntu16. You can run the code simply by typing "python main.py", and change the settings using argparse. The test function is still under construction, but I believe this code is easy to read, and it will not be difficult to implement it yourself.

Here are results after 20000, 40000, 60000, 80000 and 100000 iterstions. The results are not very satisfying, and front hair is a serious problem. I will go ong trying to fine-tuning this model (and train with scenery dataset.)

![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/19999.png?raw=true)

Result after 20000 iterations

![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/39999.png?raw=true)

Result after 40000 iterations

![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/59999.png?raw=true)

Result after 60000 iterations

![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/79999.png?raw=true)

Result after 80000 iterations

![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/99999.png?raw=true)

Result after 100000 iterations

I also added some test results here:

![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/53.png?raw=true)

![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/58.png?raw=true)

![alt text](https://github.com/SystemErrorWang/CartoonGAN/blob/master/results/74.png?raw=true)

