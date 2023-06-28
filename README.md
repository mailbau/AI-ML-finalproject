# Machine Learning Final Project - White Wine Analysis
This repository contains the code and documentation for my group's final machine learning project for our Artificial Intelligence course, where we performed analysis on a white wine dataset using various machine learning algorithms, data augmentation techniques, and statistical analyses.

## Dataset
We used a white wine dataset for this project. Dataset source: https://archive.ics.uci.edu/dataset/186/wine+quality

## Algorithms
We employed the following machine learning algorithms for regression tasks:

- Regression Tree
- Polynomial Regression
- XGBoost

## Data Augmentation with GAN
To enhance the dataset, we applied data augmentation using Generative Adversarial Networks (GAN). This technique helps generate synthetic data that can expand the diversity and size of the original dataset.

## Feature Selection with Backward Elimination
To identify the most relevant features for the regression task, we applied backward elimination. This technique iteratively removes features that contribute the least to the model's performance, ultimately selecting the most significant ones.

## Performance Comparison Before and After Data Augmentation
I evaluated the performance of each algorithm before and after data augmentation. To quantify the improvement, we performed a paired t-test to compare the performance of each algorithm, before and after augmentation.

## Performance Comparison After Data Augmentation
After data augmentation, we compared the performance of each algorithm using a one-way ANOVA test. This statistical analysis allowed us to assess the significance of performance differences among the algorithms after augmentation.

## Repository Structure

Here's a brief overview of the repository's structure:

- AIProject.ipynb                  (the actual project with all the code)
- data/                                      (folder containing the dataset and generated data)
   - winequality-white.csv        (the dataset we used)
   - trained_generated_model.h5  (generated fake data model)
   - output.csv                           (fake data after being turned into a CSV file)
   - combined_csv.csv               (combined CSV file of raw data and fake data)
   - aftergan.csv                       (combined data after running GAN for the first time, combining raw data and generated data)
   - dfganselected.csv               (data after data augmentation and feature selection)

- README.md                            (this file providing an overview of the project)

## Usage

To reproduce the results, follow the instructions below:

1. Clone this repository:

   ```shell
   git clone https://github.com/your-username/your-repo.git
2. Upload the entire repository folder to your Google Drive.
3. Open the AIProject.ipynb notebook file using Google Colab or a Jupyter Notebook environment.
4. Make sure the necessary dependencies are installed. If required, install any missing dependencies.
5. Adjust the data and file paths in the notebook to match the paths within your Google Drive folder. For example, update the paths for winequality-white.csv, trained_generated_model.h5, output.csv, combined_csv.csv, aftergan.csv, and dfganselected.csv to reflect the correct paths within your Google Drive folder.
6. Follow the instructions within each section of the notebook to execute the code and reproduce the results. **GAN section doesn't need to be executed if you are using the data we provided (output, combined_csv, aftergan, dfganselected)**
7. Review the output files and analysis presented in the notebook to understand the reproduced results.

If you want to generate new results, including running the GAN section, follow the same steps as above but ensure that you have the required data in your Google Drive folder. Make any necessary adjustments to the notebook to account for the updated file paths.

Please note that the provided files in the repository (trained_generated_model.h5, output.csv, combined_csv.csv, aftergan.csv, dfganselected.csv) already contain the generated and combined data that we used. **File names, paths, and certain code in the notebook may need to be adjusted if you are generating new results.**

## Results

The results of the analysis are as follows:

1. **Comparison of Regression Tree Method (Before vs. After Augmentation and Feature Selection):**
   - Paired t-test: t-value = -1.512, p-value = 0.205
   - Conclusion: The p-value (0.205) is greater than the significance level of 0.05. Therefore, we do not have enough evidence to reject the null hypothesis. There is no significant difference in accuracy between the regression tree method before and after applying data augmentation and feature selection.

2. **Comparison of Polynomial Regression Method (Before vs. After Augmentation and Feature Selection):**
   - Paired t-test: t-value = -1.166, p-value = 0.308
   - Conclusion: The p-value (0.308) is greater than the significance level of 0.05. Hence, we fail to reject the null hypothesis. There is no statistically significant difference in accuracy between the polynomial regression method before and after data augmentation and feature selection.

3. **Comparison of XGBoost Method (Before vs. After Augmentation and Feature Selection):**
   - Paired t-test: t-value = 0.597, p-value = 0.5832
   - Conclusion: The p-value (0.5832) is higher than the significance level. Therefore, we cannot reject the null hypothesis. There is no significant difference in accuracy observed between the XGBoost method before and after applying data augmentation and feature selection.

4. **Comparison of Classifiers (After Augmentation and Feature Selection):**
   - Null hypothesis (H0): There is no significant difference in accuracy between the classifiers after combining data augmentation and feature selection.
   - Alternate hypothesis (H1): There is a significant difference in accuracy between the classifiers after combining data augmentation and feature selection.
   - ANOVA: F-value = 573.68, p-value = 0.999
   - Conclusion: The p-value (0.999) is much larger than the significance level of 0.05. Therefore, we do not have enough evidence to reject the null hypothesis. Based on the statistical analysis, we cannot conclude that there is a significant difference between the classifiers after combining data augmentation and feature selection.
  
## Conclusion

In conclusion, our project highlights the importance of data augmentation and feature selection in addressing data scarcity issues. Although these techniques did not lead to significant improvements in performance individually or when comparing the methods, they provided valuable insights into feature relevance and ensured robustness of the models. The findings emphasize the need for carefully selecting appropriate modeling techniques and indicate that the original methods, along with data augmentation and feature selection, can effectively predict white wine quality.
