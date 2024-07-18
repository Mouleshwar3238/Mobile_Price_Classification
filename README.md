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
      <td align="center">50.750</td>
      <td align="center">53.574</td>
      <td align="center">50.750</td>
      <td align="center">51.798</td>
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
      <td align="center">70.062</td>
      <td align="center">71.743</td>
      <td align="center">70.062</td>
      <td align="center">70.098</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">48.250</td>
      <td align="center">51.798</td>
      <td align="center">48.250</td>
      <td align="center">48.543</td>
    </tr>
    <tr>
      <td align="center" colspan="6"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>5</strong></td>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">69.688</td>
      <td align="center">70.784</td>
      <td align="center">69.688</td>
      <td align="center">69.731</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">53.000</td>
      <td align="center">56.822</td>
      <td align="center">53.000</td>
      <td align="center">54.012</td>
    </tr>
    <tr>
      <td align="center" colspan="6"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>10</strong></td>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">66.625</td>
      <td align="center">67.381</td>
      <td align="center">66.625</td>
      <td align="center">66.777</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">56.250</td>
      <td align="center">58.742</td>
      <td align="center">56.250</td>
      <td align="center">56.903</td>
    </tr>
    <tr>
      <td align="center" colspan="6"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>20</strong></td>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">69.812</td>
      <td align="center">70.253</td>
      <td align="center">69.812</td>
      <td align="center">69.955</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">59.250</td>
      <td align="center">62.209</td>
      <td align="center">59.250</td>
      <td align="center">60.084</td>
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
      <td align="center">95.000</td>
      <td align="center">95.040</td>
      <td align="center">95.000</td>
      <td align="center">94.489</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">83.250</td>
      <td align="center">83.327</td>
      <td align="center">83.250</td>
      <td align="center">83.263</td>
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
      <td align="center">90.250</td>
      <td align="center">90.218</td>
      <td align="center">90.250</td>
      <td align="center">90.226</td>
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
      <td align="center">81.938</td>
      <td align="center">82.112</td>
      <td align="center">81.938</td>
      <td align="center">82.016</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">79.750</td>
      <td align="center">80.613</td>
      <td align="center">79.750</td>
      <td align="center">79.942</td>
    </tr>
  </tbody>
  </table>

## Linear SVC (Support Vector Classifier)
For the linear SVC model, the optimal hyperparameters were found using halving grid search with 5-fold cross validation, and confusion matrices and bar plots were plotted for the corresponding results.
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
      <td align="center">96.000</td>
      <td align="center">96.001</td>
      <td align="center">96.000</td>
      <td align="center">95.999</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">97.750</td>
      <td align="center">97.771</td>
      <td align="center">97.750</td>
      <td align="center">97.746</td>
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
      <td align="center">98.375</td>
      <td align="center">98.375</td>
      <td align="center">98.375</td>
      <td align="center">98.375</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">97.500</td>
      <td align="center">97.624</td>
      <td align="center">97.500</td>
      <td align="center">97.507</td>
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
      <td align="center">98.438</td>
      <td align="center">98.440</td>
      <td align="center">98.438</td>
      <td align="center">98.436</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">97.500</td>
      <td align="center">97.582</td>
      <td align="center">97.500</td>
      <td align="center">97.506</td>
    </tr>
  </tbody>
  </table>

## Linear Discriminant Analysis (LDA)
For the LDA model, the optimal hyperparameters were found using halving grid search with 5-fold cross validation, and confusion matrices and bar plots were plotted for the corresponding results.
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
      <td align="center">95.062</td>
      <td align="center">95.162</td>
      <td align="center">95.062</td>
      <td align="center">95.090</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">94.500</td>
      <td align="center">94.859</td>
      <td align="center">94.500</td>
      <td align="center">94.554</td>
    </tr>
  </tbody>
  </table>

## Perceptron
For the perceptron model, the optimal hyperparameters were found using halving grid search with 5-fold cross validation, and confusion matrices and bar plots were plotted for the corresponding results.
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
      <td align="center">87.625</td>
      <td align="center">87.299</td>
      <td align="center">87.625</td>
      <td align="center">87.410</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">88.000</td>
      <td align="center">87.923</td>
      <td align="center">88.000</td>
      <td align="center">87.857</td>
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
      <td align="center">93.000</td>
      <td align="center">92.825</td>
      <td align="center">92.800</td>
      <td align="center">92.788</td>
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
      <td align="center">92.500</td>
      <td align="center">92.466</td>
      <td align="center">92.293</td>
      <td align="center">92.304</td>
    </tr>
    <tr>
      <td align="center" colspan="6"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>Sigmoid</strong></td>
      <td align="center"><strong>Training Subset</strong></td>
      <td align="center">99.688</td>
      <td align="center">99.696</td>
      <td align="center">99.690</td>
      <td align="center">99.692</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">96.500</td>
      <td align="center">94.523</td>
      <td align="center">96.562</td>
      <td align="center">96.437</td>
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
      <td align="center">91.250</td>
      <td align="center">91.521</td>
      <td align="center">91.250</td>
      <td align="center">91.289</td>
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
      <td align="center">90.000</td>
      <td align="center">90.036</td>
      <td align="center">90.000</td>
      <td align="center">90.017</td>
    </tr>
    <tr>
      <td align="center"><strong>Test Subset</strong></td>
      <td align="center">90.750</td>
      <td align="center">91.022</td>
      <td align="center">90.750</td>
      <td align="center">90.798</td>
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
      <td align="center">91.000</td>
      <td align="center">91.148</td>
      <td align="center">91.000</td>
      <td align="center">91.026</td>
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
      <td align="center">90.000</td>
      <td align="center">90.227</td>
      <td align="center">90.000</td>
      <td align="center">90.053</td>
    </tr>
  </tbody>
  </table>

## XGBoost Classifier
For the XGBoost classifier, the optimal hyperparameters were found using halving grid search with 5-fold cross validation, and confusion matrices and bar plots were plotted for the corresponding results.
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
      <td align="center">90.743</td>
      <td align="center">90.750</td>
      <td align="center">90.732</td>
    </tr>
  </tbody>
  </table>

(Note:- Though Linear SVC and SVC use the same kernel, they use different solvers and the latter is preferred over the former for bigger datasets)
