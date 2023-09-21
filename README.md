# Contexual-Biasing-Dataset

paper: [CB-Conformer: Contextual biasing Conformer for biased word recognition](https://arxiv.org/pdf/2304.09607)

This repository contains the Mandarin biased words dataset with five sub-datasets, namely the person-name dataset, the place-name dataset, the organization-name dataset, and the full set of biased words containing all categories called "all_biased" dataset as well as the dataset without biased words called "no_biased" dataset.

Each sub-dataset is divided into train, test, and dev sets, and contains a collection of biased words. The specific dataset sizes are as follows:

|              | train    | dev  | test  | time(h) | number of biased words |
| ------------ | -------- | ---- | ----- | ------- | ---------------------- |
| person-name  | 1000     | 1000 | 9997  | 10.24   | 73                     |
| place-name   | 1000     | 1000 | 10191 | 12.96   | 42                     |
| organization | 1000     | 500  | 2035  | 3.94    | 183                    |
| all_biased   | 2992     | 2497 | 21972 | 26.77   | 298                    |
| no_biased    | 12774458 | /    | /     | 793.30  | /                      |

This dataset is filtered and divided from the WenetSpeech dataset, if you need to use this dataset, you need to do the following steps
1. download the 

   [WenetSpeech]: https://wenet.org.cn/WenetSpeech/	""WenetSpeech""

    dataset

2. Save the wav.scp from WenetSpeech/WenetSpeech/train_m or your own wav.scp to each sub-dataset

3. Call fix_data_dir.sh of the 

   [Kaldi]: https://github.com/kaldi-asr/kaldi	""Kaldi""

    tool to process each sub-dataset and you will get a filtered and constructed dataset


citation:
```
@inproceedings{CB-Conformer,
  title={CB-Conformer: Contextual biasing Conformer for biased word recognition},
  author={Xu, Yaoxun and Liu, Baiji and Huang, Qiaochu and Song, Xingchen and Wu, Zhiyong and Kang, Shiyin and Meng, Helen},
  booktitle={ICASSP 2023-2023 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)},
  pages={1--5},
  year={2023},
  organization={IEEE}
}
```