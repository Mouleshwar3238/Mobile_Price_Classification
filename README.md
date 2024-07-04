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

The dataset has been split into a training subset and test subset, with 80 % being used for training and 20 % being used for testing. The algorithms have been run on the original data as well as on the normalized data, with the latter being normalized using StandardScaler.

## K Nearest Neighbours (KNN Classifier)
For the KNN algorithm, the accuracy rates were computed for different values of K and the confusion matrix was plotted for some of these values.
* Best Value of K
  <table>
  <thead>
    <tr>
      <th align="center"></th>
      <th align="center">Original Data</th>
      <th align="center">Normalized Data</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><strong>Value of K</strong></td>
      <td align="center">10</td>
      <td align="center">49</td>
    </tr>
    <tr>
      <td align="center"><strong>Accuracy Rate (in %)</strong></td>
      <td align="center">92.75</td>
      <td align="center">63.00</td>
    </tr>
  </tbody>
  </table>
* Other Values of K
  <table>
  <thead>
    <tr>
      <th align="center">Value of K</th>
      <th align="center">Accuracy Rate (in %) <br> for Original Data</th>
      <th align="center">Accuracy Rate (in %) <br> for Normalized Data</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center">3</td>
      <td align="center">92.25</td>
      <td align="center">45.75</td>
    </tr>
    <tr>
      <td align="center">5</td>
      <td align="center">92.00</td>
      <td align="center">49.25</td>
    </tr>
    <tr>
      <td align="center">20</td>
      <td align="center">91.50</td>
      <td align="center">59.50</td>
    </tr>
    <tr>
      <td align="center">50</td>
      <td align="center">90.75</td>
      <td align="center">63.25</td>
    </tr>
  </tbody>
  </table>
