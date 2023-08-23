# SPCSE
The implementation code of SPCSE. 

## Results on STS Tasks

| Model                                                                                                                    | STS12      | STS13      | STS14      | STS15      | STS16      | STSb       | SICK-R     | Avg.       |
|--------------------------------------------------------------------------------------------------------------------------|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|
| [unsup-spcse-bert-base](https://huggingface.co/ilingen/unsup-spcse-bert-base)  | 72.80 | 83.82 | 76.00 | 83.11 | 79.78 | 80.07 |71.34 | 78.13 |
| [unsup-spcse-bert-large](https://huggingface.co/ilingen/unsup-spcse-bert-large) | 73.85 | 85.83 | 77.68 | 85.05 | 79.17 | 80.79 | 75.04 | 79.63 |
## Results on Transfer Tasks

# Setup

Install Dependencies
``` sh
pip install -r requirements.txt
```
## Generate Augmented Sentence
To simplify our training process, instead of augmenting the sentence during training, we choose to first generate the augmented sentence.
First, we need to download the raw sentence in SimCSE.
``` sh
cd SPCSE/data
bash download_wiki.sh
```
Next, Augment the raw sentence.
Based on EDA's work, for each sentence, we generate 4 augmented sentences.
``` sh
python get_augment_sents.py
```
## Training
Our training process is the same as SimCSE, and the following parameters are required for training.


# Evaluation

To evaluate our SPCSE, please run the following script
``` sh
python evaluation.py --model_name_or_path ilingen/unsup-spcse-bert-base --pooler cls_before_pooler
```
# Train

Our training code, data will be available soon.
