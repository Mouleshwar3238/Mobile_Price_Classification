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
      <td align="center"><strong>Accuracy Rate (in %) </strong></td>
      <td align="center">93.75</td>
      <td align="center">61.00</td>
    </tr>
  </tbody>
  </table>
* Other Values of K
  <table>
  <thead>
    <tr>
      <th align="center">Value of K</th>
      <th align="center">Accuracy Rate (in %) <br> for Original Test Data</th>
      <th align="center">Accuracy Rate (in %) <br> for Normalized Test Data</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center">3</td>
      <td align="center">92.00</td>
      <td align="center">41.50</td>
    </tr>
    <tr>
      <td align="center">5</td>
      <td align="center">92.00</td>
      <td align="center">45.25</td>
    </tr>
    <tr>
      <td align="center">20</td>
      <td align="center">93.75</td>
      <td align="center">59.50</td>
    </tr>
    <tr>
      <td align="center">40</td>
      <td align="center">93.00</td>
      <td align="center">61.00</td>
    </tr>
  </tbody>
  </table>
The accuracy rates for the original data were quite high compared to that of the normalized data.

## Support Vector Classifier (SVC)
A SVC was implemented using differenet kernels and confusion matrices were plotted for the corresponding results.
* Cross Validation
  <table>
  <thead>
    <tr>
      <th align="center">SVC Kernel</th>
      <th align="center">Accuracy Rate (in %) <br> for Original Data</th>
      <th align="center">Accuracy Rate (in %) <br> for Normalized Data</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center">Linear</td>
      <td align="center">97.25</td>
      <td align="center">95.38</td>
    </tr>
    <tr>
      <td align="center">Polynomial</td>
      <td align="center">95.44</td>
      <td align="center">75.62</td>
    </tr>
    <tr>
      <td align="center">RBF</td>
      <td align="center">95.19</td>
      <td align="center">86.44</td>
    </tr>
    <tr>
      <td align="center">Sigmoid</td>
      <td align="center">19.75</td>
      <td align="center">91.12</td>
    </tr>
  </tbody>
  </table>

* Test Dataset
  <table>
  <thead>
    <tr>
      <th align="center">SVC Kernel</th>
      <th align="center">Accuracy Rate (in %) <br> for Original Data</th>
      <th align="center">Accuracy Rate (in %) <br> for Normalized Data</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center">Linear</td>
      <td align="center">97.00</td>
      <td align="center">97.00</td>
    </tr>
    <tr>
      <td align="center">Polynomial</td>
      <td align="center">96.25</td>
      <td align="center">78.75</td>
    </tr>
    <tr>
      <td align="center">RBF</td>
      <td align="center">96.50</td>
      <td align="center">89.25</td>
    </tr>
    <tr>
      <td align="center">Sigmoid</td>
      <td align="center">17.50</td>
      <td align="center">92.25</td>
    </tr>
  </tbody>
  </table>

For the linear, polynomial and rbf kernels, the accuracy rates remained the same or decreased after normalizing the data. On the other hand, for the sigmoid kernel, the accuracy rates improved by a huge extent after normalizing the data.
