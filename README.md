# Mobile_Price_Classification
Implemented some popular classification algorithms to classify the price range of mobile phones. (Extensive improvements were carried out later)

## Dataset Description
The dataset contains features for about 2000 mobile phones, as well as their appropriate price range depending on the metrics for these features. There are 4 different classes for the prices (low, medium, high and very high)
* Title: Mobile Price Classification
* URL: https://www.kaggle.com/datasets/iabhishekofficial/mobile-price-classification
<table>
<thead>
  <tr>
    <th align="center" colspan="2">Generic Description</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td align="center">Number of samples</td>
    <td align="center">2,000</td>
  </tr>
  <tr>
    <td align="center">Number of attributes</td>
    <td align="center">21</td>
  </tr>
  <tr>
    <td align="center">Input features</td>
    <td align="center">20 (battery power, clock speed, <br> height, weight etc.)</td>
  </tr>
  <tr>
    <td align="center">Target variable</td>
    <td align="center">price_range (0 to 3)</td>
  </tr>
</tbody>
</table>

The dataset was split into a training subset and test subset, with 80 % being used for training and 20 % being used for testing. Before being used, the data in both subsets was normalized using StandardScaler.

## K Nearest Neighbours (KNN Classifier)
For the KNN classifier, the accuracy rates were computed for different values of K for the training dataset, and confusion matrices and bar plots were plotted for some of these values to visualize the frequency distribution of actual and predicted labels for the test dataset.
* Best Value of K (= 1)
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">90.750</td>
      <td align="center">90.750</td>
      <td align="center">90.750</td>
      <td align="center">90.744</td>
    </tr>
  </tbody>
  </table>

* Other Values of K
  <table>
  <thead>
    <tr>
      <th align="center">Value of K</th>
      <th align="center"></th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="2"><strong>3</strong></td>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">96.062</td>
      <td align="center">96.063</td>
      <td align="center">96.062</td>
      <td align="center">96.062</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">93.750</td>
      <td align="center">93.716</td>
      <td align="center">93.750</td>
      <td align="center">93.703</td>
    </tr>
    <tr>
      <td align="center" colspan="6"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>5</strong></td>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">94.250</td>
      <td align="center">94.259</td>
      <td align="center">94.250</td>
      <td align="center">94.249</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">92.750</td>
      <td align="center">92.736</td>
      <td align="center">92.750</td>
      <td align="center">92.721</td>
    </tr>
    <tr>
      <td align="center" colspan="6"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>10</strong></td>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">94.062</td>
      <td align="center">94.109</td>
      <td align="center">94.062</td>
      <td align="center">94.060</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">95.250</td>
      <td align="center">95.302</td>
      <td align="center">95.250</td>
      <td align="center">95.248</td>
    </tr>
  </tbody>
  </table>

## Decision Tree Classifier
For the decision tree model, the optimal hyperparameters were found using halving grid search with 5-fold cross validation, and confusion matrices and bar plots were plotted for the corresponding results.
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">97.312</td>
      <td align="center">97.349</td>
      <td align="center">97.312</td>
      <td align="center">97.320</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">83.250</td>
      <td align="center">83.368</td>
      <td align="center">83.250</td>
      <td align="center">83.298</td>
    </tr>
  </tbody>
  </table>

## Random Forest Classifier
For the random forest model, the optimal hyperparameters were found using halving grid search with 5-fold cross validation, and confusion matrices and bar plots were plotted for the corresponding results.
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">86.250</td>
      <td align="center">86.076</td>
      <td align="center">86.250</td>
      <td align="center">86.139/td>
    </tr>
  </tbody>
  </table>

## Gaussian Naive Bayes Classifier
For the Gaussian Naive Bayes model, the optimal hyperparameters were found using halving grid search with 5-fold cross validation, and confusion matrices and bar plots were plotted for the corresponding results.
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">81.625</td>
      <td align="center">82.683</td>
      <td align="center">81.625</td>
      <td align="center">82.643</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">83.500</td>
      <td align="center">83.415</td>
      <td align="center">83.500</td>
      <td align="center">83.441</td>
    </tr>
  </tbody>
  </table>

## SVM (Support Vector Machine)
For the SVM model, the optimal hyperparameters were found using halving grid search with 5-fold cross validation, and confusion matrices and bar plots were plotted for the corresponding results.
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">98.250</td>
      <td align="center">98.254</td>
      <td align="center">98.250</td>
      <td align="center">98.251</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">94.250</td>
      <td align="center">94.220</td>
      <td align="center">94.250</td>
      <td align="center">94.227</td>
    </tr>
  </tbody>
  </table>

## Logistic Regression
For the logistic regression model, the optimal hyperparameters were found using halving grid search with 5-fold cross validation, and confusion matrices and bar plots were plotted for the corresponding results.
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">99.250</td>
      <td align="center">99.251</td>
      <td align="center">99.250</td>
      <td align="center">99.250</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">96.500</td>
      <td align="center">96.512</td>
      <td align="center">96.500</td>
      <td align="center">96.498</td>
    </tr>
  </tbody>
  </table>

## SGD (Stochastic Gradient Descent) Classifier
For the SGD classifier, the optimal hyperparameters were found using halving grid search with 5-fold cross validation, and confusion matrices and bar plots were plotted for the corresponding results.
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">91.188</td>
      <td align="center">91.188</td>
      <td align="center">91.188</td>
      <td align="center">91.188</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">88.250</td>
      <td align="center">88.394</td>
      <td align="center">88.250</td>
      <td align="center">88.314</td>
    </tr>
  </tbody>
  </table>

## Neural Network
A neural network with 3 hidden layers was implemented using different activation functions, and confusion matrices and bar plots were plotted for the corresponding results.
  <table>
  <thead>
    <tr>
      <th align="center">Activation Function</th>
      <th align="center"></th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="2"><strong>ReLU</strong></td>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">91.750</td>
      <td align="center">91.635</td>
      <td align="center">91.635</td>
      <td align="center">91.627</td>
    </tr>
    <tr>
      <td align="center" colspan="6"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>Tanh</strong></td>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">94.000</td>
      <td align="center">93.964</td>
      <td align="center">93.983</td>
      <td align="center">93.971</td>
    </tr>
    <tr>
      <td align="center" colspan="6"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>Sigmoid</strong></td>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">99.562</td>
      <td align="center">99.568</td>
      <td align="center">99.570</td>
      <td align="center">99.568</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">95.000</td>
      <td align="center">94.967</td>
      <td align="center">94.809</td>
      <td align="center">94.872</td>
    </tr>
  </tbody>
  </table>

## AdaBoost Classifier
For the AdaBoost classifier model, the optimal hyperparameters were found using halving grid search with 5-fold cross validation, and confusion matrices and bar plots were plotted for the corresponding results.
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">92.250</td>
      <td align="center">92.201</td>
      <td align="center">92.250</td>
      <td align="center">92.213</td>
    </tr>
  </tbody>
  </table>

## Histogram-based Gradient Boosting Classifier
For the gradient boosting classifier, the optimal hyperparameters were found using halving grid search with 5-fold cross validation, and confusion matrices and bar plots were plotted for the corresponding results.
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
      <td align="center">100.000</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">91.750</td>
      <td align="center">91.831</td>
      <td align="center">91.750</td>
      <td align="center">91.782</td>
    </tr>
  </tbody>
  </table>

## Bagging Classifier
For the bagging classifier, the optimal hyperparameters were found using halving grid search with 5-fold cross validation, and confusion matrices and bar plots were plotted for the corresponding results.
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">99.625</td>
      <td align="center">99.626</td>
      <td align="center">99.625</td>
      <td align="center">99.625</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">89.750</td>
      <td align="center">89.809</td>
      <td align="center">89.750</td>
      <td align="center">89.771</td>
    </tr>
  </tbody>
  </table>

(Note:- Though Linear SVC and SVC use the same kernel, they use different solvers and the latter is preferred over the former for bigger datasets)
