## Data Preparation
This repository keeps a data preparation tool for datasets in [insightface/Dataset-Zoo](https://github.com/deepinsight/insightface/wiki/Dataset-Zoo). It convert `mxnet.recordio` files (`.idx` `.rec`) and binary files (`.bin`) into `.jpg` and `.npy` format files for Pytorch usage. We take the well known MS1M-ArcFace(MS1MV2) dataset for example in the following steps.

## Usage

### Step 1. Download dataset.

Download the MS1M-ArcFace(MS1MV2) dataset and unzip files into data/ directory.

```
$ cd data/
$ wget https://dl.dropbox.com/s/wpx6tqjf0y5mf6r/faces_ms1m-refine-v2_112x112.zip?dl=1
$ unzip faces_ms1m-refine-v2_112x112.zip?dl=1
```
- [MS1M-ArcFace @ BaiduDrive](https://pan.baidu.com/s/1S6LJZGdqcZRle1vlcMzHOQ)
- [MS1M-ArcFace @ Dropbox](https://www.dropbox.com/s/wpx6tqjf0y5mf6r/faces_ms1m-refine-v2_112x112.zip?dl=0)
- for more Dataset please refer to the [original post](https://github.com/deepinsight/insightface/wiki/Dataset-Zoo)

**Note:** If you use the refined [MS-Celeb-1M](https://arxiv.org/abs/1607.08221) dataset and the cropped [VGG2](https://arxiv.org/abs/1710.08092) dataset, please cite the original papers.

### Step 2. Prepare Dataset

- After unzip the files to 'data' path, run :

  ```
  $ python prepare_data.py
  ```

  after the execution, you should find following structure:

  ```
  ├─ prepare_data.py
  └─ data/
        └─ faces_emore/
                ├─ agedb_30/
                ├─ calfw/
                ├─ cfp_ff/
                ├─ cfp_fp/
                ├─ cplfw/
                ├─ imgs/       # ms1m-arcface dataset
                ├─ lfw/
                └─ vgg2_fp/
  ```
 
- For other datasets, please add `-r` args for the record path:

  ```
  $ python prepare_data.py -r faces_webface_112x112/
  ```
