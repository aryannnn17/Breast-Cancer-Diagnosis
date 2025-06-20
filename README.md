<header><h1> Supervised, Semi-Supervised and Unsupervised Learning </h1>
</header>

<main>
<section>
<h4> Download Dataset: https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic
 </h4>
 <p> Dataset has IDs, classes (Benign=B, Malignant=M), and 30 attributes. This data has two output classes. Use the first 20% of the positive and negative classes in the file as the test set and the rest as the training set.</p>

<h3>Quesion:</h3>

<div>  Monte-Carlo Simulation: Repeat the following procedures for supervised, un- supervised, and semi-supervised learning M = 30 times, and use randomly se- lected train and test data (make sure you use 20% of both the positve and nega- tive classes as the test set). Then compare the average scores (accuracy, precision, recall, F-score, and AUC) that you obtain from each algorithm.</div>

<ol> 
    <li>
    Supervised Learning: Train an L 1 -penalized SVM to classify the data. Use 5 fold cross validation to choose the penalty parameter. Use normalized data. Report the average accuracy, precision, recall, F-score, and AUC, for both training and test sets over your M runs. Plot the ROC and report the confusion matrix for training and testing in one of the runs.
    </li>
    <li>
    Semi-Supervised Learning/ Self-training: select 50% of the positive class along with 50% of the negative class in the training set as labeled data and the rest as unlabelled data. You can select them randomly.<ul>
    <li>Train an L 1 -penalized SVM to classify the labeled data Use normalized data. Choose the penalty parameter using 5 fold cross validation.</li>
    <li>Find the unlabeled data point that is the farthest to the decision boundary of the SVM. Let the SVM label it (ignore its true label), and add it to the labeled data, and retrain the SVM. Continue this process until all unlabeled data are used. Test the final SVM on the test data andthe average accuracy, precision, recall, F-score, and AUC, for both training and test sets over your M runs. Plot the ROC and report the confusion matrix for training and testing in one of the runs.</li>
    </ul>
    </li>
    <li>
    Unsupervised Learning: Run k-means algorithm on the whole training set. Ignore the labels of the data, and assume k = 2.<ul>
    <li>Run the k-means algorithm multiple times. Make sure that you initialize the algoritm randomly. How do you make sure that the algorithm was not trapped in a local minimum?</li>
    <li>Compute the centers of the two clusters and find the closest 30 data points to each center. Read the true labels of those 30 data points and take a majority poll within them. The majority poll becomes the label predicted by k-means for the members of each cluster. Then compare the labels provided by k-means with the true labels of the training data and report the average accuracy, precision, recall, F-score, and AUC over M runs, and ROC and the confusion matrix for one of the runs.</li>
    <li>Classify test data based on their proximity to the centers of the clusters. Report the average accuracy, precision, recall, F-score, and AUC over M runs, and ROC and the confusion matrix for one of the runs for the test data.</li>
    </ul>
    </li>
     <li>
    Spectral Clustering: Repeat 1(b)iii using spectral clustering, which is clus- tering based on kernels. Research what spectral clustering is. Use RBF kernel.</li>
</ol>
</section>
</main>
