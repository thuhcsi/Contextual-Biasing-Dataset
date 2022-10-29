# Contexual-Biasing-Dataset

This repository contains the Mandarin biased words dataset with five sub-datasets, namely the person-name dataset, the place-name dataset, the organization-name dataset, and the full set of biased words containing all categories called "all_biased" dataset as well as the dataset without biased words called "no_biased" dataset.

Each sub-dataset is divided into train, test, and dev sets, and contains a collection of biased words. The specific dataset sizes are as follows:

![image-20221029150216544](C:\Users\99476\AppData\Roaming\Typora\typora-user-images\image-20221029150216544.png)

This dataset is filtered and divided from the WenetSpeech dataset, if you need to use this dataset, you need to do the following steps
1. download the WenetSpeech dataset
2. Save the wav.scp from WenetSpeech/WenetSpeech/train_m or your own wav.scp to each sub-dataset
3. Call fix_data_dir.sh of the kaldi tool to process each sub-dataset and you will get a filtered and constructed dataset
