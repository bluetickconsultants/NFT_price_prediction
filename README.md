<h1 align="center">   Price Predictions for NFT Images </h1>

<hr>

<div align="center">
  <img src="https://user-images.githubusercontent.com/88481845/215969419-2a1f3ce2-de6f-4954-8fbf-6808ddd2e999.png">
</div>

<hr>


An NFT is an image in the form of a digital token. These tokens are then sold online. AN NFT can be anything in digital form. Every NFT image has its own price and we implement Machine learning techniques to predict the price for the NFT images. 

For implementing this problem statement we collected the images and related prices using selenium script around 5000 images from Multiple sources. To extract the information from all the images we used OpenCV and NumPy and we collected the pixel intensities from every image. Hence there are in RGB color space we converted 3-dimensional data into one dimensional which works as independent data for machine learning Algorithms and Prices of each image as a dependent feature. 

# Techniques used

• Numpy
• Pandas
• Seaborn
• Matplotlib
• Statistics
• Opencv
• Machine learning Supervised techniques

<img src="https://user-images.githubusercontent.com/88481845/215969710-0c5e1e38-3915-4a11-8994-7e3dcc6f6a46.png">

Using NumPy and pandas we removed the unwanted image which does not carry any kind of information. Hence we are having Independent and dependent features we used Machine learning supervised techniques Like regression and classification_regression Algorithms. 

<hr>

# Algorithms used

• Multiple Linear Regression
• KNN Regressor
• Support Vector machine Regressor
• Adaboost Regressor
• Decision Tree

For training the data for ML Algorithms we split the data into train and test where the training part has 80% of the data and the test part has 20% of the data.

We trained KNN Regressor, support vector Regressor and Decision tree, and Adaboost Regressor but unfortunately, the results are not so good because KNN needs to collect perfect k-values since the problem is Regression, not a classification so due to the distribution range of values from independent data is too high.

For the support vector machine due to high dimensionality in the data marginal distance and support vectors are very close to each other so we are facing an over-fitting problem while implementing the support vector machine.

## Multiple Linear Regression

<img src="https://user-images.githubusercontent.com/88481845/215970036-e71851c2-3412-43a1-adc2-83014c6d8743.png" width="40%">

Hence Multiple linear regression is a regression technique and the result are going better when compare to KNN-R and SVM-R. Initially, the train accuracy for the MLR model was 91 and 82 for the test. So we find out to improve the performance of the model using feature engineering and Regularization techniques.


## Handling Outliers for MLR

Hence the data features are more in size there is no option for us to select the best features because each and every pixel is important that carries the information. so using sci-kit learn and feature engine we handled outliers using the 5th quantile and 95th quantile area which makes to remove the small amount of data which are far away from the remaining data points.
 
<img src="https://user-images.githubusercontent.com/88481845/215970306-805219c5-ead6-49b7-bc6e-88d6122c93d3.png">

Feature scaling for MLR:

We clear the outliers and there are some features following skewness and some features not following Normal Distribution. Using the feature engine framework we scale down the pixel values using standardization and using yeo johnson transformation we handled skewness to follow Normal Distribution. Hence yeo johnson transformation has no impact on the negative values this technique helps us to handle data.

Even though we handled outliers and skewness of the data. The increase in the test accuracy is not so high so we collected more images and increase the data size. so to check whether the newly added data gives better results or not we implement adjusted r2 techniques just to check the model performance before adding the data and after adding the data. Adding the data really helps us but not is a big scale. so we went to handle the overfitting problems using regularization techniques like L1 and L2 techniques.

Using this Ridge and Lasso regression we reduce the bias on small scale and increase variance on small scale by updating the coefficient values. Updating the values of the coefficients and making errors close to Zero increased the model Performace.
So in the end accuracy value for train and test is

• Training Accuracy = 98.052948845
• Test Accuracy = 89.674529872


<hr>

# Output

<table>
  <tbody>
  <tr>
  <th>Images</th>
  <th>Actual Price</th>
  <th>Predicted Price by MLR Model</th>
  </tr>
    <tr>
      <td align="center">
        <img src="https://user-images.githubusercontent.com/88481845/215970987-3eb86a7c-18cc-4543-8398-c09644daa220.png" width="40%">
      </td>
      <td>$176</td>
      <td>$144</td>
    </tr>
     <tr>
      <td align="center">
        <img src="https://user-images.githubusercontent.com/88481845/215971628-5d1958f9-7e83-41a2-8ba9-005695a3214d.png" width="40%">
      </td>
      <td>$89</td>
      <td>$119</td>
    </tr>
    <tr>
      <td align="center">
        <img src="https://user-images.githubusercontent.com/88481845/215971701-fb282bb7-b36a-4e30-920e-bd27242ac0f5.png" width="40%">
      </td>
      <td>$212</td>
      <td>$254</td>
    </tr>
    <tr>
      <td align="center">
        <img src="https://user-images.githubusercontent.com/88481845/215971864-aa631685-69c2-4a9c-98cc-5ee8c6d636eb.png" width="40%">
      </td>
      <td>$143</td>
      <td>$189</td>
    </tr>
    <tr>
      <td align="center">
        <img src="https://user-images.githubusercontent.com/88481845/215972003-c4bd184d-f897-477d-b9c8-517ea0e34cf1.png" width="40%">
      </td>
      <td>$2,939.50</td>
      <td>$3,159.88</td>
    </tr>
  </tbody>
</table>



## Useful Information

### References
- [Price Predictions for NFT Images ](https://www.bluetickconsultants.com/price-predictions-for-nft-images.html)

## Other Projects

To view all other open source projects visit
  - [ Open Source Projects ](https://www.bluetickconsultants.com/open-source.html) 
  - [ Open Source Repositories ](https://github.com/orgs/bluetickconsultants/repositories)

## Author

[Bluetick Consultants LLP](https://www.bluetickconsultants.com/)
  #### contact us at admin@bluetickconsultants.com
  
<img src="https://user-images.githubusercontent.com/88481845/215745914-16aa10a5-f24b-4fa9-b1be-432454487788.png" width="50%">

