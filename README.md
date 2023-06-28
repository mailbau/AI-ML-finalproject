# Machine Learning Final Project - White Wine Analysis
This repository contains the code and documentation for my group's final machine learning project for our Artificial Intelligence course, where we performed analysis on a white wine dataset using various machine learning algorithms, data augmentation techniques, and statistical analyses.

## Summary
We used a white wine dataset for this project. Dataset source: https://archive.ics.uci.edu/dataset/186/wine+quality

We employed the following machine learning algorithms for regression tasks:
- Regression Tree
- Polynomial Regression
- XGBoost

Data is augmented with Generative Adversarial Networks (GAN) and feature selection using backward elimination.
We then create performance comparisons:
- Performance Comparison Before and After Data Augmentation (we performed a paired t-test to compare the performance of each algorithm, before and after augmentation)
- Performance Comparison After Data Augmentation (we performed one-way ANOVA test to compare the performance differences among the algorithms after augmentation)

## Usage

To reproduce the results, follow the instructions below:

1. Clone this repository:

   ```shell
   git clone https://github.com/mailbau/AI-ML-finalproject.git
2. Upload the entire repository folder to your Google Drive.
3. Open the AIProject.ipynb notebook file using Google Colab or a Jupyter Notebook environment.
4. Make sure the necessary dependencies are installed. If required, install any missing dependencies.
5. Adjust the data and file paths in the notebook to match the paths within your Google Drive folder. For example, update the paths for winequality-white.csv, trained_generated_model.h5, output.csv, combined_csv.csv, aftergan.csv, and dfganselected.csv to reflect the correct paths within your Google Drive folder.
6. Follow the instructions within each section of the notebook to execute the code and reproduce the results. **GAN section doesn't need to be executed if you are using the data we provided (output, combined_csv, aftergan, dfganselected)**
7. Review the output files and analysis presented in the notebook to understand the reproduced results.

If you want to generate new results, including running the GAN section, follow the same steps as above but ensure that you have the required data in your Google Drive folder. Make any necessary adjustments to the notebook to account for the updated file paths.

Please note that the provided files in the repository (trained_generated_model.h5, output.csv, combined_csv.csv, aftergan.csv, dfganselected.csv) already contain the generated and combined data that we used. **File names, paths, and certain code in the notebook may need to be adjusted if you are generating new results.**

## Results and Conclusion

Please see the [Results and Conclusion](./docs/results.md) document for a comprehensive analysis of the results and our final conclusions.
