# SPCSE
The implementation code of SPCSE. 

## Results on STS Tasks

| Model                                                                                                                    | STS12      | STS13      | STS14      | STS15      | STS16      | STSb       | SICK-R     | Avg.       |
|--------------------------------------------------------------------------------------------------------------------------|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|
| [unsup-spcse-bert-base](https://huggingface.co/ilingen/unsup-spcse-bert-base)  | 72.80 | 83.82 | 76.00 | 83.11 | 79.78 | 80.07 |71.34 | 78.13 |
| [unsup-spcse-bert-large](https://huggingface.co/ilingen/unsup-spcse-bert-large) | 73.85 | 85.83 | 77.68 | 85.05 | 79.17 | 80.79 | 75.04 | 79.63 |
# Setup

Install Dependencies
``` sh
pip install -r requirements.txt
```
# Evaluation

To evaluate our SPCSE, please run the following script
``` sh
python evaluation.py --model_name_or_path ilingen/unsup-spcse-bert-base --pooler cls_before_pooler
```
# Train

Our training code, data will be available soon.
