# Soliciting User Preferences in Conversational Recommender Systems via Usage-related Questions

This repository provides resources developed within the following article:

> I. Kostric, K. Balog and F. Radlinski. **Soliciting User Preferences in Conversational Recommender Systems via Usage-related Questions** In: RecSys '21: Fifteenth ACM Conference on Recommender Systems.     Association for Computing Machinery, New York, NY, United States. September 2021. [DOI: 10.1145/3460231.3478861](https://doi.org/10.1145/3460231.3478861) [PDF](https://arxiv.org/pdf/2111.13463.pdf)

## Summary

A key distinguishing feature of conversational recommender systems over traditional recommender systems is their ability to elicit user preferences using natural language. Currently, the predominant approach to preference elicitation is to ask questions directly about items or item attributes. These strategies do not perform well in cases where the user does not have sufficient knowledge of the target domain to answer such questions. Conversely, in a shopping setting, talking about the planned use of items does not present any difficulties, even for those that are new to a domain. In this paper, we propose a novel approach to preference elicitation by asking implicit questions based on item usage. Our approach consists of two main steps. First, we identify the sentences from a large review corpus that contain information about item usage. Then, we generate implicit preference elicitation questions from those sentences using a neural text-to-text model. The main contributions of this work also include a multi-stage data annotation protocol using crowdsourcing for collecting high-quality labeled training data for the neural model. We show that out approach is effective in selecting review sentences and transforming them to elicitation questions, even with limited training data.

## Repository Structure

This repository is structured as follows:

- `dataset/`: Train/test datasets collected via crowdsourcing. **NB! The files do not contain the original review text and extracted sentences.**

- `code/make_dataset.py`: A Python script for populating the dataset with original review text and extracted sentences.

## Obtaining the dataset

To obtain the full dataset use command:

```
python -m code.make_dataset --path <path_to_amazon_collection_folder>
```

The script expects files `Patio_Lawn_and_Garden.json.gz`, `Home_and_Kitchen.json.gz`, and `Sports_and_Outdoors.json.gz` to be present in the `<path_to_amazon_collection_folder>`. It parses through the files and populates the datasets with the original review and sentence texts.
The outputs are saved as `train_full.csv` and `test_full.csv` in the dataset folder.

## Citation

If you use the resources presented in this repository, please cite:

```
@inbook{10.1145/3460231.3478861,
  author = {Kostric, Ivica and Balog, Krisztian and Radlinski, Filip},
  title = {Soliciting User Preferences in Conversational Recommender Systems via Usage-Related Questions},
  booktitle = {Fifteenth ACM Conference on Recommender Systems},
  year = {2021},
  pages = {724--729},
  doi = {10.1145/3460231.3478861}
  publisher = {Association for Computing Machinery}
}
```

## Contact

Should you have any questions, please contact Ivica Kostric at ivica.kostric@uis.no.
