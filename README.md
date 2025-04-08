# Senti-Persian-Dataset

**Senti-Persian** is a novel Sentiment Analysis (SA) dataset in Persian, designed to address the challenges of low-resource languages by leveraging advanced data augmentation techniques. This dataset includes 67,743 public comments from Iranian websites (Namava, Filimo, Aparat) and social media platforms (YouTube, Twitter, Instagram), annotated with sentiment labels: **positive**, **negative**, and **neutral**.

## Key Features

- **Size**: 67,743 labeled movie review comments.
- **Sources**: Comments are collected from popular Iranian websites (Namava, Filimo, Aparat) and social media platforms (YouTube, Twitter, Instagram).
- **Sentiment Labels**: Each comment is labeled as **positive**, **negative**, or **neutral**.
- **Data Augmentation**: Includes synthetic data generated using a Generative Adversarial Network (GAN)-based approach, specifically designed for Persian linguistics.
- **Performance Boost**: When used with the augmented dataset, sentiment analysis models achieve a significant improvement in accuracy—from **88.4%** (original dataset) to **96%** (augmented dataset).

## Data Augmentation Methodology

The dataset incorporates a novel text augmentation model based on GANs:
- **Generator**: Designed to follow the linguistic properties of Persian.
- **Discriminator**: Evaluates the quality of synthetic data using cosine similarity of vectorized sentences (CLS-embeddings from BERT).

This method ensures that the augmented data maintains semantic consistency with the original dataset while increasing its volume and variety.

## Usage

The dataset is available in two versions:
1. **Original Dataset**: Contains the raw, manually annotated comments.
2. **Augmented Dataset**: Includes both the original comments and synthetic data generated via the GAN-based augmentation technique.To use the dataset, download it from the following link:

[Google Drive - Senti-Persian Dataset](https://drive.google.com/file/d/1HgM84w6SBxbiTXlmKstI_r9CTGXjFN41/view?usp=sharing)


You can download the dataset from this repository and use it for training and evaluating sentiment analysis models.

## Results

| Dataset Version       | Accuracy |
|-----------------------|----------|
| Original Dataset      | 88.4%    |
| Augmented Dataset     | 96%      |

These results demonstrate the effectiveness of our GAN-based augmentation method in improving model performance.

## Paper
For more details about the methodology and experiments, please refer to the accompanying research paper:

[Boosting Sentiment Analysis in Persian through a GAN-Based Synthetic Data Augmentation Method
](https://aclanthology.org/2025.abjadnlp-1.7/)
## Citation

If you use this dataset in your research, please cite the following paper:

```bibtex
@inproceedings{mohammadi-etal-2025-boosting,
    title = "Boosting Sentiment Analysis in {P}ersian through a {GAN}-Based Synthetic Data Augmentation Method",
    author = "Mohammadi, Masoumeh  and
      Amin, Mohammad Ruhul  and
      Tavakoli, Shadi",
    editor = "El-Haj, Mo",
    booktitle = "Proceedings of the 1st Workshop on NLP for Languages Using Arabic Script",
    month = jan,
    year = "2025",
    address = "Abu Dhabi, UAE",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.abjadnlp-1.7/",
    pages = "54--63"
}
```


## Repository Contents

- `data/original/`: Contains the original dataset (raw comments and annotations).
- `data/augmented/`: Contains the augmented dataset (original + synthetic data).
- `scripts/`: Includes scripts for preprocessing and utilizing the dataset.
- `README.md`: This file.

## License

This dataset is released under the [MIT License](LICENSE). Feel free to use, modify, and distribute it for research and development purposes.

## Contact

For questions or feedback, please contact:
- Masoumeh Mohammadi: mohammadi.masou@gmail.com
- Mohammad Ruhul Amin: mamin17@fordham.edu
- Shadi Tavakoli:tavakoli.shadii@gmail.com
