# Master's thesis - Think Twice Before You Answer: Mitigating Biases of Question Answering Models

## Student: Lukáš Mikula

## Advisor: Mgr. Michal Štefánik

This GitHub repository stores source code and datasets for the master's thesis.

This work is implemented in Python, at first, please, install the requrements.txt [requrements.txt](requrements.txt) file with the standard command:

```bash
pip install -r requirements.txt
```

#### All the source code is available in the form of Jupyter Notebooks, all these Notebooks are in the main directory:

[BERT_base_finetuning.ipynb](BERT_base_finetuning.ipynb) - for baseline BERT-base-uncased model fine-tuning on SQuAD dataset.

[computation_of_heuristics.ipynb](computation_of_heuristics.ipynb) - for computation of our proposed heuristics on SQuAD

[measuring_bias_significance.ipynb](measuring_bias_significance.ipynb) - for measuring the bias significance by bootstrap on dataset with predictions

[evaluation_of_models_on_multiple_datasets.ipynb](evaluation_of_models_on_multiple_datasets.ipynb) - for evaluation of saved fine-tuned BERT models on validation datasets

[formatting_of_validation_datasets.ipynb](formatting_of_validation_datasets.ipynb) - for postprocessing of Natural Questions and TriviaQA datasets to SQuAD-like structure

[BERT_debiased_models_finetuning.ipynb](BERT_debiased_models_finetuning.ipynb) - for fine-tuning of BERT models on super-sampled training dataset

[BERT_finetuning_with_validation_losses.ipynb](BERT_finetuning_with_validation_losses.ipynb) - for evaluation of out-of-domain datasets' losses during BERT fine-tuning

We run all notebooks for BERT fine-tuning on Kaggle, because the fine-tuning demands a powerful GPU. However, the paths to the datasets are altered to work with this structure. If you want to run these notebooks On Colab or Kaggle, please, change the paths in corresponding cells.

#### The datasets, we use in our experiments and evaluations are available in directory [datasets](./datasets/) in .json format:

[valid_squad_with_predictions.json](./datasets/valid_squad_with_predictions.json) - validation SQuAD with predicted answers from the baseline BERT model

[squad_train.json](./datasets/squad_train.json) - train SQuAD in .json format, for fitting od TF-IDF

[squad_train_with_heuristics_flags.json](./datasets/squad_train_with_heuristics_flags.json)

[enhanced_valid_squad_with_predictions.json](./datasets/enhanced_valid_squad_with_predictions.json) - validation SQuAD with predicted answers from the baseline BERT model and computed heuristics

[nq_dev.json](./datasets/nq_dev.json) - validation Natural Questions dataset obtained by the [QA dataset converter](https://github.com/amazon-research/qa-dataset-converter)

[nq_dev_formatted.json](./datasets/nq_dev_formatted.json) - validation Natural Questions dataset with postprocessing to SQuAD-like format

[triviaqa_dev.json](./datasets/triviaqa_dev.json) - validation TriviaQA dataset obtained by the [QA dataset converter](https://github.com/amazon-research/qa-dataset-converter)

[triviaqa_dev_formatted.json](./datasets/triviaqa_dev_formatted.json) - validation TriviaQA dataset with postprocessing to SQuAD-like format

[adversarialqa_validation.json](./datasets/adversarialqa_validation.json) - validation AdversarialQA dataset in .json format
