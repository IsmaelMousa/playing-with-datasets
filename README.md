# Hugging Face Datasets Practice

## Overview
This repository is designed for practicing the use of Hugging Face **datasets**.

## Objectives
- Learn to load **datasets** from the **Hugging Face** hub using various methods.
- Explore techniques for preparing **datasets**.
- Understand different tokenization, batching, and padding techniques.
- Identify and choose suitable **datasets** from the **Hugging Face** hub.
- Practice applying preprocessing to real raw data from A to Z.
  - > [!NOTE]
    > 
    > Here I used raw wikipedia dataset and applying the preprocessing operations such as:
      > 1. Removing unnecessary columns.
      > 2. Shuffling data.
      > 3. Computing article body lengths.
      > 4. Filtering content.
      > 5. Cleaning HTML character codes.
      > 6. Converting between Datasets and DataFrames.
      > 7. Splitting the data into training and testing sets.

## Usage
1. Clone this repository to your local machine:
```zsh
git clone git@github.com:IsmaelMousa/playing-with-datasets.git
```
2. Navigate to the **playing-with-datasets** directory:
```zsh
cd playing-with-datasets
```
3. Setup virtual environment:
```zsh
python3 -m venv .venv
```
4. Activate the virtual environment:

```zsh
source .venv/bin/activate
```
5. Install the required dependencies:

```zsh
pip install -r requirements.txt
```

6. Run the Notebook:
```zsh
jupyter-notebook
```

## Dataset

The dataset used is a raw wikipedia dataset stored in Parquet format.

## Processing Steps

1. **Load the Dataset**: Load the dataset from a Parquet file.

2. **Remove Unnecessary Columns**: Drop columns such as `URL`, `Introduction/Summary`, `Sections/Headings`, `References`, `Categories`, and `Infobox`.

3. **Shuffle the Dataset**: Shuffle the dataset using a seed for reproducibility.

4. **Compute Article Body Length**: Calculate the word count for the `Body` of each article.

5. **Filter Out Empty and Short Articles**: Remove articles with empty bodies or fewer than 30 words.

6. **Clean HTML Character Codes**: Convert HTML character codes to plain text.

7. **Convert Between Datasets and DataFrames**: Convert the dataset to a Pandas DataFrame for easier manipulation, then convert it back to a dataset.

8. **Split the Dataset**: Split the dataset into `training` (70%) and `testing` (30%) sets.

9. **Save the Processed Dataset**: Save the processed dataset in various formats such as JSONL, CSV, and Parquet.

10. **Test Loading the Processed Dataset**: Load the saved datasets to ensure they are correctly formatted and usable.
