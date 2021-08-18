# DeepFakeMnist+

This page contain the download link for our proposed data DeepFake Mnist+, [download link](https://1fichier.com/?xva635m3whdgcae2k81q).

# Dataset Introdution

It contains video animation data generated by [First Order Motion Model for Image Animation](https://papers.nips.cc/paper/2019/file/31c0b36aef265d9221af80872ceb62f9-Paper.pdf)

The dataset contain 10,000 real videos selected from [VoxCeleb1](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/vox1.html) and 10,000 animation videos generated by using these 10,000 real videos as sources.

![alt text](https://github.com/huangjiadidi/DeepFakeMnist/blob/main/readme_src/action_clip.png)

Image animation means given a victim's image, and a driving video (which provide action), the animation result is a video that the victim perform same action just like the driving video did. 

The animation videos is animated with 10 different actions, including: Blink, Open mouth, Yaw, Nod, Right slope head, Left slope head, Look up and smile, surprise and embarrassment. The driving videos with different actions are collected by multiple actors. In addition, we select the embarrassment videos from [ADFES](https://aice.uva.nl/research-tools/adfes-stimulus-set/adfes-stimulus-set.html?cb) as the driving videos for embarrassment. We generated 1000 videos for each action.

In order to select high-quality animation video, all generated videos have passed and able to proof the recent liveness detectors in the markets. We select the two detectors from [Baidu](https://ai.baidu.com/tech/face/faceliveness) and [Tianyan](https://www.tianyandata.cn/) to help us to filter out the high-quailty results.

# Dataset Evaluation

*Accuracy under different network and compression level*


|                     | Resnet50  | Resnet101 | Resnet152 | XceptionNet | MesoNet |
| :-----------------: |:---------:| :--------:| :--------:| :----------:| :------:|
| raw                 | 96.58%    | 96.64%    | 96.18%    | 92.38%      | 60.39%  |
| light compression   | 94.32%    | 94.87%    | 94.90%    | 85.52%      | 58.58%  |
| heavy compression   | 91.49%    | 90.44%    | 91.27%    | 83.14%      | 57.90%  |

notes: **raw** means original videos, light compression means the videos are compressed with H.264 in c23 compression ratio, heavy compression means the videos are compressed with H.264 in c40 compression ratio.




