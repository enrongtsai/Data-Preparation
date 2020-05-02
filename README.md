## Data Preparation
This repository keeps a data preparation tool for converting `.bin` `.idx` `.rec` files in the MS1M-refine-v2 (emore) dataset into images.

## Usage

### Step 1. Download dataset.

Download the MS1M-refine-v2(emore) dataset and unzip files into dataset/ directory.

```
cd dataset/
wget https://dl.dropbox.com/s/wpx6tqjf0y5mf6r/faces_ms1m-refine-v2_112x112.zip?dl=1
unzip faces_ms1m-refine-v2_112x112.zip?dl=1
```
- [emore dataset @ BaiduDrive](https://pan.baidu.com/s/1eXohwNBHbbKXh5KHyItVhQ)
- [emore dataset @ Dropbox](https://www.dropbox.com/s/wpx6tqjf0y5mf6r/faces_ms1m-refine-v2_112x112.zip?dl=0)
- for more Dataset please refer to the [original post](https://github.com/deepinsight/insightface/wiki/Dataset-Zoo)

**Note:** If you use the refined [MS1M](https://arxiv.org/abs/1607.08221) dataset and the cropped [VGG2](https://arxiv.org/abs/1710.08092) dataset, please cite the original papers.

### Step 2. Prepare Dataset

- after unzip the files to 'dataset' path, run :

  ```
  python3 prepare_data.py
  ```

  after the execution, you should find following structure:

  ```
  ├─ prepare_data.py
  └─ dataset/
        └─ faces_emore/
                ├─ agedb_30/
                ├─ calfw/
                ├─ cfp_ff/
                ├─ cfp_fp/
                ├─ cplfw/
                ├─ imgs/
                ├─ lfw/
                └─ vgg2_fp/
  ```
