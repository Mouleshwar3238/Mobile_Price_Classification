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
