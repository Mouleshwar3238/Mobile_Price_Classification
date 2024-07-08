# Mobile_Price_Classification
Implemented some popular classification algorithms to classify the price range of mobile phones.

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

The dataset has been split into a training subset and test subset, with 80 % being used for training and 20 % being used for testing. The algorithms have been run on the original data as well as on the normalized data, with the latter being normalized using StandardScaler. K-fold cross validation with 5 folds (K = 5) was used to validate the performance of all the models.

## K Nearest Neighbours (KNN Classifier)
For the KNN algorithm, the accuracy rates were computed for different values of K for the training dataset, and confusion matrices and bar plots were plotted for some of these values to visualize the frequency distribution of actual and predicted labels for the test dataset.
* Best Value of K
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Original Test Data</th>
      <th align="center">Normalized Test Data</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><strong>Value of K</strong></td>
      <td align="center">11</td>
      <td align="center">50</td>
    </tr>
    <tr>
      <td align="center"><strong>Accuracy (in %)</strong></td>
      <td align="center">96.000</td>
      <td align="center">61.000</td>
    </tr>
    <tr>
      <td align="center"><strong>Precision (in %)</strong></td>
      <td align="center">96.024</td>
      <td align="center">60.828</td>
    </tr>
    <tr>
      <td align="center"><strong>Recall (in %)</strong></td>
      <td align="center">96.026</td>
      <td align="center">61.629</td>
    </tr>
    <tr>
      <td align="center"><strong>F1 Score (in %)</strong></td>
      <td align="center">96.007</td>
      <td align="center">61.116</td>
    </tr>
  </tbody>
  </table>
  
* Other Values of K
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Value of K</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="4"><strong>Original Test Data</strong></td>
      <td align="center">3</td>
      <td align="center">93.500</td>
      <td align="center">93.515</td>
      <td align="center">93.545</td>
      <td align="center">93.522</td>
    </tr>
    <tr>
      <td align="center">5</td>
      <td align="center">94.250</td>
      <td align="center">94.314</td>
      <td align="center">94.300</td>
      <td align="center">94.300</td>
    </tr>
    <tr>
      <td align="center">20</td>
      <td align="center">94.750</td>
      <td align="center">94.750</td>
      <td align="center">94.807</td>
      <td align="center">94.774</td>
    </tr>
    <tr>
      <td align="center">40</td>
      <td align="center">94.250</td>
      <td align="center">94.233</td>
      <td align="center">94.314</td>
      <td align="center">94.265</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="4"><strong>Normalized Test Data</strong></td>
      <td align="center">3</td>
      <td align="center">45.750</td>
      <td align="center">46.711</td>
      <td align="center">46.734</td>
      <td align="center">45.564</td>
    </tr>
    <tr>
      <td align="center">5</td>
      <td align="center">47.500</td>
      <td align="center">48.458</td>
      <td align="center">48.354</td>
      <td align="center">47.957</td>
    </tr>
    <tr>
      <td align="center">20</td>
      <td align="center">53.250</td>
      <td align="center">53.037</td>
      <td align="center">54.065</td>
      <td align="center">53.376</td>
    </tr>
    <tr>
      <td align="center">40</td>
      <td align="center">60.750</td>
      <td align="center">60.280</td>
      <td align="center">61.476</td>
      <td align="center">60.701</td>
    </tr>
  </tbody>
  </table>

## Support Vector Classifier (SVC)
A SVC was implemented using differenet kernels, and confusion matrices and bar graphs were plotted for the corresponding results.
* Cross Validation
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Kernel</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="4"><strong>Original Data</strong></td>
      <td align="center">Linear</td>
      <td align="center">97.250</td>
      <td align="center">97.274</td>
      <td align="center">97.285</td>
      <td align="center">97.264</td>
    </tr>
    <tr>
      <td align="center">Polynomial</td>
      <td align="center">95.438</td>
      <td align="center">95.513</td>
      <td align="center">95.478</td>
      <td align="center">95.454</td>
    </tr>
    <tr>
      <td align="center">RBF</td>
      <td align="center">95.188</td>
      <td align="center">95.259</td>
      <td align="center">95.223</td>
      <td align="center">95.215</td>
    </tr>
    <tr>
      <td align="center">Sigmoid</td>
      <td align="center">19.750</td>
      <td align="center">23.051</td>
      <td align="center">19.919</td>
      <td align="center">21.063</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="4"><strong>Normalized Data</strong></td>
      <td align="center">Linear</td>
      <td align="center">95.375</td>
      <td align="center">95.480</td>
      <td align="center">95.435</td>
      <td align="center">95.429</td>
    </tr>
    <tr>
      <td align="center">Polynomial</td>
      <td align="center">75.625</td>
      <td align="center">77.889</td>
      <td align="center">75.660</td>
      <td align="center">76.307</td>
    </tr>
    <tr>
      <td align="center">RBF</td>
      <td align="center">86.437</td>
      <td align="center">86.954</td>
      <td align="center">86.499</td>
      <td align="center">86.644</td>
    </tr>
    <tr>
      <td align="center">Sigmoid</td>
      <td align="center">91.125</td>
      <td align="center">91.316</td>
      <td align="center">91.167</td>
      <td align="center">91.194</td>
    </tr>
  </tbody>
  </table>
  
* Test Dataset
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Kernel</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="4"><strong>Original Data</strong></td>
      <td align="center">Linear</td>
      <td align="center">97.000</td>
      <td align="center">97.023</td>
      <td align="center">96.990</td>
      <td align="center">96.920</td>
    </tr>
    <tr>
      <td align="center">Polynomial</td>
      <td align="center">96.250</td>
      <td align="center">96.156</td>
      <td align="center">96.143</td>
      <td align="center">96.137</td>
    </tr>
    <tr>
      <td align="center">RBF</td>
      <td align="center">96.500</td>
      <td align="center">96.368</td>
      <td align="center">96.551</td>
      <td align="center">96.439</td>
    </tr>
    <tr>
      <td align="center">Sigmoid</td>
      <td align="center">17.500</td>
      <td align="center">19.977</td>
      <td align="center">16.878</td>
      <td align="center">18.141</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="4"><strong>Normalized Data</strong></td>
      <td align="center">Linear</td>
      <td align="center">97.000</td>
      <td align="center">97.086</td>
      <td align="center">96.975</td>
      <td align="center">96.916</td>
    </tr>
    <tr>
      <td align="center">Polynomial</td>
      <td align="center">78.750</td>
      <td align="center">79.024</td>
      <td align="center">78.436</td>
      <td align="center">78.483</td>
    </tr>
    <tr>
      <td align="center">RBF</td>
      <td align="center">89.250</td>
      <td align="center">88.969</td>
      <td align="center">88.958</td>
      <td align="center">88.886</td>
    </tr>
    <tr>
      <td align="center">Sigmoid</td>
      <td align="center">92.250</td>
      <td align="center">92.016</td>
      <td align="center">92.079</td>
      <td align="center">92.027</td>
    </tr>
  </tbody>
  </table>

## Decision Tree Classifier
A decision tree classifier was implemented using different impurity measures (entropy and gini index), and confusion matrices and bar graphs were plotted for the corresponding results.
* Cross Validation
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Criterion</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="2"><strong>Original Data</strong></td>
      <td align="center">Entropy</td>
      <td align="center">85.062</td>
      <td align="center">85.186</td>
      <td align="center">85.178</td>
      <td align="center">85.068</td>
    </tr>
    <tr>
      <td align="center">Gini Index</td>
      <td align="center">82.812</td>
      <td align="center">82.965</td>
      <td align="center">82.948</td>
      <td align="center">82.857</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>Normalized Data</strong></td>
      <td align="center">Entropy</td>
      <td align="center">85.062</td>
      <td align="center">85.186</td>
      <td align="center">85.178</td>
      <td align="center">85.068</td>
    </tr>
    <tr>
      <td align="center">Gini Index</td>
      <td align="center">82.812</td>
      <td align="center">82.966</td>
      <td align="center">82.948</td>
      <td align="center">82.857</td>
    </tr>
  </tbody>
  </table>
  
* Test Dataset
  <table>
  <thead>
    <tr>
     <tr>
      <th align="center"></th>
      <th align="center">Criterion</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="2"><strong>Original Data</strong></td>
      <td align="center">Entropy</td>
      <td align="center">85.000</td>
      <td align="center">85.101</td>
      <td align="center">84.829</td>
      <td align="center">84.747</td>
    </tr>
    <tr>
      <td align="center">Gini Index</td>
      <td align="center">83.250</td>
      <td align="center">82.942</td>
      <td align="center">82.720</td>
      <td align="center">82.671</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>Normalized Data</strong></td>
      <td align="center">Entropy</td>
      <td align="center">85.000</td>
      <td align="center">85.101</td>
      <td align="center">84.829</td>
      <td align="center">84.747</td>
    </tr>
    <tr>
      <td align="center">Gini Index</td>
      <td align="center">83.750</td>
      <td align="center">83.474</td>
      <td align="center">83.266</td>
      <td align="center">83.214</td>
    </tr>
  </tbody>
  </table>

## AdaBoost Classifier
An AdaBoost Classifier was implemented using different base estimators, and confusion matrices and bar graphs were plotted for the corresponding results.
* Cross Validation
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Base Estimator</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="4"><strong>Original Data</strong></td>
      <td align="center">Decision Tree</td>
      <td align="center">91.687</td>
      <td align="center">91.831</td>
      <td align="center">91.735</td>
      <td align="center">91.744</td>
    </tr>
    <tr>
      <td align="center">Logistic Regression</td>
      <td align="center">75.562</td>
      <td align="center">76.591</td>
      <td align="center">75.673</td>
      <td align="center">75.967</td>
    </tr>
    <tr>
      <td align="center">Linear SVC</td>
      <td align="center">71.938</td>
      <td align="center">73.350</td>
      <td align="center">72.027</td>
      <td align="center">72.443</td>
    </tr>
    <tr>
      <td align="center">Gaussian Naive Bayes</td>
      <td align="center">89.250</td>
      <td align="center">89.894</td>
      <td align="center">89.275</td>
      <td align="center">89.414</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="4"><strong>Normalized Data</strong></td>
      <td align="center">Decision Tree</td>
      <td align="center">91.687</td>
      <td align="center">91.831</td>
      <td align="center">91.735</td>
      <td align="center">91.744</td>
    </tr>
    <tr>
      <td align="center">Logistic Regression</td>
      <td align="center">95.625</td>
      <td align="center">95.754</td>
      <td align="center">95.651</td>
      <td align="center">95.658</td>
    </tr>
    <tr>
      <td align="center">Linear SVC</td>
      <td align="center">92.688</td>
      <td align="center">92.798</td>
      <td align="center">92.745</td>
      <td align="center">92.693</td>
    </tr>
    <tr>
      <td align="center">Gaussian Naive Bayes</td>
      <td align="center">89.938</td>
      <td align="center">90.279</td>
      <td align="center">89.991</td>
      <td align="center">90.047</td>
    </tr>
  </tbody>
  </table>
  
* Test Dataset
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Base Estimator</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="4"><strong>Original Data</strong></td>
      <td align="center">Decision Tree</td>
      <td align="center">91.000</td>
      <td align="center">90.842</td>
      <td align="center">90.875</td>
      <td align="center">90.774</td>
    </tr>
    <tr>
      <td align="center">Logistic Regression</td>
      <td align="center">77.750</td>
      <td align="center">78.254</td>
      <td align="center">77.491</td>
      <td align="center">77.607</td>
    </tr>
    <tr>
      <td align="center">Linear SVC</td>
      <td align="center">74.000</td>
      <td align="center">75.451</td>
      <td align="center">73.865</td>
      <td align="center">74.089</td>
    </tr>
    <tr>
      <td align="center">Gaussian Naive Bayes</td>
      <td align="center">91.250</td>
      <td align="center">91.173</td>
      <td align="center">91.293</td>
      <td align="center">91.129</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="4"><strong>Normalized Data</strong></td>
      <td align="center">Decision Tree</td>
      <td align="center">91.000</td>
      <td align="center">90.842</td>
      <td align="center">90.875</td>
      <td align="center">90.774</td>
    </tr>
    <tr>
      <td align="center">Logistic Regression</td>
      <td align="center">96.500</td>
      <td align="center">96.416</td>
      <td align="center">96.537</td>
      <td align="center">96.450</td>
    </tr>
    <tr>
      <td align="center">Linear SVC</td>
      <td align="center">93.000</td>
      <td align="center">92.923</td>
      <td align="center">92.832</td>
      <td align="center">92.805</td>
    </tr>
    <tr>
      <td align="center">Gaussian Naive Bayes</td>
      <td align="center">91.250</td>
      <td align="center">91.183</td>
      <td align="center">91.293</td>
      <td align="center">91.118</td>
    </tr>
  </tbody>
  </table>

## Logistic Regression Classifier
A logistic regression classifier was implemented using different penalty terms, and confusion matrices and bar graphs were plotted for the corresponding results. The best value of the regularization parameter C was chosen by computing the performance metrics for different values of C and plotting a graph for the former versus the latter.
* Cross Validation
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Penalty Term</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="2"><strong>Original Data</strong></td>
      <td align="center">L1</td>
      <td align="center">85.625</td>
      <td align="center">85.686</td>
      <td align="center">85.909</td>
      <td align="center">85.716</td>
    </tr>
    <tr>
      <td align="center">L2</td>
      <td align="center">81.875</td>
      <td align="center">81.506</td>
      <td align="center">82.219</td>
      <td align="center">81.738</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>Normalized Data</strong></td>
      <td align="center">L1</td>
      <td align="center">85.750</td>
      <td align="center">86.002</td>
      <td align="center">86.020</td>
      <td align="center">85.929</td>
    </tr>
    <tr>
      <td align="center">L2</td>
      <td align="center">85.500</td>
      <td align="center">85.541</td>
      <td align="center">85.790</td>
      <td align="center">85.570</td>
    </tr>
  </tbody>
  </table>
  
* Test Dataset
  <table>
  <thead>
    <tr>
     <tr>
      <th align="center"></th>
      <th align="center">Penalty Term</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="2"><strong>Original Data</strong></td>
      <td align="center">L1</td>
      <td align="center">88.250</td>
      <td align="center">87.505</td>
      <td align="center">87.343</td>
      <td align="center">87.384</td>
    </tr>
    <tr>
      <td align="center">L2</td>
      <td align="center">84.750</td>
      <td align="center">83.469</td>
      <td align="center">83.567</td>
      <td align="center">83.447</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>Normalized Data</strong></td>
      <td align="center">L1</td>
      <td align="center">88.250</td>
      <td align="center">87.598</td>
      <td align="center">87.376</td>
      <td align="center">87.429</td>
    </tr>
    <tr>
      <td align="center">L2</td>
      <td align="center">88.250</td>
      <td align="center">87.505</td>
      <td align="center">87.343</td>
      <td align="center">87.384</td>
    </tr>
  </tbody>
  </table>

## Gaussian Naive Bayes Classifier
A Gaussian Naive Bayes classifier was implemented with prior probabilities being set as the probabilities of each class in the dataset, and confusion matrices and bar graphs were plotted for the corresponding results.
* Cross Validation
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
      <td align="center"><strong>Original Data</strong></td>
      <td align="center">79.875</td>
      <td align="center">80.324</td>
      <td align="center">80.072</td>
      <td align="center">80.116</td>
    <tr>
      <td align="center"><strong>Normalized Data</strong></td>
      <td align="center">79.938</td>
      <td align="center">80.370</td>
      <td align="center">80.136</td>
      <td align="center">80.174</td>
    </tr>
  </tbody>
  </table>
  
* Test Dataset
  <table>
  <thead>
    <tr>
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
      <td align="center"><strong>Original Data</strong></td>
      <td align="center">80.250</td>
      <td align="center">80.268</td>
      <td align="center">79.919</td>
      <td align="center">79.748</td>
    </tr>
    <tr>
      <td align="center"><strong>Normalized Data</strong></td>
      <td align="center">80.250</td>
      <td align="center">80.268</td>
      <td align="center">79.919</td>
      <td align="center">79.948</td>
    </tr>
  </tbody>
  </table>

## Multi-Layer Perceptron
An Multi-Layer Perceptron classifier was implemented with 50 nodes in the hidden layer with different activation functions, and confusion matrices and bar graphs were plotted for the corresponding results.
* Cross Validation
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Activation Function</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="3"><strong>Original Data</strong></td>
      <td align="center">Logistic/Sigmoid</td>
      <td align="center">72.625</td>
      <td align="center">73.228</td>
      <td align="center">72.809</td>
      <td align="center">72.819</td>
    </tr>
    <tr>
      <td align="center">Tanh</td>
      <td align="center">63.062</td>
      <td align="center">62.495</td>
      <td align="center">63.443</td>
      <td align="center">62.380</td>
    </tr>
    <tr>
      <td align="center">ReLU</td>
      <td align="center">62.438</td>
      <td align="center">64.720</td>
      <td align="center">62.783</td>
      <td align="center">60.682</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="3"><strong>Normalized Data</strong></td>
      <td align="center">Logistic/Sigmoid</td>
      <td align="center">94.562</td>
      <td align="center">94.656</td>
      <td align="center">94.612</td>
      <td align="center">94.596</td>
    </tr>
    <tr>
      <td align="center">Tanh</td>
      <td align="center">93.812</td>
      <td align="center">93.906</td>
      <td align="center">93.868</td>
      <td align="center">93.860</td>
    </tr>
    <tr>
      <td align="center">ReLU</td>
      <td align="center">90.938</td>
      <td align="center">91.066</td>
      <td align="center">91.000</td>
      <td align="center">90.991</td>
    </tr>
  </tbody>
  </table>
  
* Test Dataset
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Activation Function</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="3"><strong>Original Data</strong></td>
      <td align="center">Logistic/Sigmoid</td>
      <td align="center">73.000</td>
      <td align="center">72.119</td>
      <td align="center">72.243</td>
      <td align="center">72.168</td>
    </tr>
    <tr>
      <td align="center">Tanh</td>
      <td align="center">72.000</td>
      <td align="center">72.331</td>
      <td align="center">71.157</td>
      <td align="center">71.397</td>
    </tr>
    <tr>
      <td align="center">ReLU</td>
      <td align="center">62.500</td>
      <td align="center">64.794</td>
      <td align="center">62.120</td>
      <td align="center">62.618</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="3"><strong>Normalized Data</strong></td>
      <td align="center">Logistic/Sigmoid</td>
      <td align="center">95.750</td>
      <td align="center">95.705</td>
      <td align="center">95.773</td>
      <td align="center">95.689</td>
    </tr>
    <tr>
      <td align="center">Tanh</td>
      <td align="center">96.250</td>
      <td align="center">96.236</td>
      <td align="center">96.167</td>
      <td align="center">96.162</td>
    </tr>
    <tr>
      <td align="center">ReLU</td>
      <td align="center">93.500</td>
      <td align="center">93.436</td>
      <td align="center">93.452</td>
      <td align="center">93.383</td>
    </tr>
  </tbody>
  </table>

## Random Forest Classifier
A random forest classifier was implemented using different impurity measures (entropy and gini index), and confusion matrices and bar graphs were plotted for the corresponding results. The optimal number of estimators was chosen by computing the performance metrics for different number of estimators and plotting a graph for the former versus the latter.
* Cross Validation
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Criterion</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="2"><strong>Original Data</strong></td>
      <td align="center">Entropy</td>
      <td align="center">88.188</td>
      <td align="center">88.499</td>
      <td align="center">88.281</td>
      <td align="center">88.323</td>
    </tr>
    <tr>
      <td align="center">Gini Index</td>
      <td align="center">88.062</td>
      <td align="center">88.303</td>
      <td align="center">88.151</td>
      <td align="center">88.184</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>Normalized Data</strong></td>
      <td align="center">Entropy</td>
      <td align="center">88.125</td>
      <td align="center">88.411</td>
      <td align="center">88.222</td>
      <td align="center">88.256</td>
    </tr>
    <tr>
      <td align="center">Gini Index</td>
      <td align="center">87.937</td>
      <td align="center">88.103</td>
      <td align="center">88.035</td>
      <td align="center">88.030</td>
    </tr>
  </tbody>
  </table>
  
* Test Dataset
  <table>
  <thead>
    <tr>
     <tr>
      <th align="center"></th>
      <th align="center">Criterion</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="2"><strong>Original Data</strong></td>
      <td align="center">Entropy</td>
      <td align="center">90.000</td>
      <td align="center">89.633</td>
      <td align="center">89.633</td>
      <td align="center">89.633</td>
    </tr>
    <tr>
      <td align="center">Gini Index</td>
      <td align="center">89.000</td>
      <td align="center">88.722</td>
      <td align="center">88.719</td>
      <td align="center">88.683</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>Normalized Data</strong></td>
      <td align="center">Entropy</td>
      <td align="center">90.500</td>
      <td align="center">90.170</td>
      <td align="center">90.183</td>
      <td align="center">890.172</td>
    </tr>
    <tr>
      <td align="center">Gini Index</td>
      <td align="center">88.750</td>
      <td align="center">88.447</td>
      <td align="center">88.498</td>
      <td align="center">88.441</td>
    </tr>
  </tbody>
  </table>

## Gradient Boosting Classifier
A gradient boosting classifier was implemented using different criterion, and confusion matrices and bar graphs were plotted for the corresponding results. The optimal number of estimators was chosen by computing the performance metrics for different number of estimators and plotting a graph for the former versus the latter.
* Cross Validation
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Criterion</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="2"><strong>Original Data</strong></td>
      <td align="center">Friedman MSE</td>
      <td align="center">90.625</td>
      <td align="center">90.773</td>
      <td align="center">90.684</td>
      <td align="center">90.699</td>
    </tr>
    <tr>
      <td align="center">Squared Error</td>
      <td align="center">90.812</td>
      <td align="center">90.925</td>
      <td align="center">90.876</td>
      <td align="center">90.884</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>Normalized Data</strong></td>
      <td align="center">Friedman MSE</td>
      <td align="center">90.750</td>
      <td align="center">90.856</td>
      <td align="center">90.815</td>
      <td align="center">90.820</td>
    </tr>
    <tr>
      <td align="center">Squared Error</td>
      <td align="center">90.750</td>
      <td align="center">90.856</td>
      <td align="center">90.815</td>
      <td align="center">90.820</td>
    </tr>
  </tbody>
  </table>
  
* Test Dataset
  <table>
  <thead>
    <tr>
     <tr>
      <th align="center"></th>
      <th align="center">Criterion</th>
      <th align="center">Accuracy (in %)</th>
      <th align="center">Precision (in %)</th>
      <th align="center">Recall (in %)</th>
      <th align="center">F1 Score (in %)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="2"><strong>Original Data</strong></td>
      <td align="center">Friedman MSE</td>
      <td align="center">91.500</td>
      <td align="center">91.240</td>
      <td align="center">91.363</td>
      <td align="center">91.279</td>
    </tr>
    <tr>
      <td align="center">Squared Error</td>
      <td align="center">92.000</td>
      <td align="center">91.772</td>
      <td align="center">91.909</td>
      <td align="center">91.818</td>
    </tr>
    <tr>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
      <td align="center"></td>
    </tr>
    <tr>
      <td align="center" rowspan="2"><strong>Normalized Data</strong></td>
      <td align="center">Friedman MSE</td>
      <td align="center">92.000</td>
      <td align="center">91.772</td>
      <td align="center">91.909</td>
      <td align="center">91.818</td>
    </tr>
    <tr>
      <td align="center">Squared Error</td>
      <td align="center">92.000</td>
      <td align="center">91.772</td>
      <td align="center">91.909</td>
      <td align="center">91.818</td>
    </tr>
  </tbody>
  </table>
