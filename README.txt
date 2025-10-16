#UJIIndoorLoc Indoor Localization Experiments
This project reproduces indoor localization experiments using the UJIIndoorLoc WiFi fingerprinting dataset. It evaluates k-NN, SVM, Decision Tree, and Gradient Boosting models, combined with PCA, to predict a building's floor based on WiFi signal strengths.

##Dataset:
This project uses the UJIIndoorLoc WiFi fingerprint dataset from KaggleHub. The notebook automatically downloads the data, which consists of 520 WAP signal strengths used to predict building floor locations.

##Experiments Conducted:
The notebook performs several experiments to evaluate model performance:

##Preprocessing: Cleans and scales WiFi signal data, then applies PCA for dimensionality reduction.
k-NN Analysis: Tests the impact of the k value, sample size, and the number of PCA components on classification error.
SVM Analysis: Compares linear vs. polynomial kernels and evaluates performance against sample size and PCA component count.
Tree-Based Models: Evaluates Decision Tree and Gradient Boosting classifiers, including an analysis of cost-complexity pruning for the Decision Tree.

##Results Summary:

1)k-NN: Performs best with a small k (1 or 3) and shows improved accuracy with more data and 50-100 PCA components.
2)SVM: A tuned polynomial kernel outperforms a linear one. Using 150 PCA components yields better results than 50.
3)Tree-Based Models: Gradient Boosting with 50 PCA components achieves over 97% accuracy. The pruned Decision Tree performs optimally with minimal pruning.

##Requirements:

numpy
pandas
matplotlib
scikit-learn
kagglehub

##How to Run
1)Clone the repository.
2)Install the required libraries.
3)Open and run ml_project.ipynb in a Jupyter environment. The notebook will automatically download the data and run the analyses.
