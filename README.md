<h1>kaggle-Rossmann-Store-Sales-Solution
</h1>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/front_page.png" width="50%" title="logo">
</p>
Rossmann operates more than 3,000 drug stores in 7 European countries. Rossmann store managers are currently responsible for forecasting their sales
daily up to six weeks in advance. In-store sales are influenced by many factors, including promotions, competition,
school holidays, seasons and locality. accuracy and results can vary considerably.
The purpose of this project is to construct, compare and evaluate models
to better predict the sales of 1115 "Rossmann" stores.
<h2> Outils : </h2>
Python : Sickit-Learn, Keras, Matplotlib, Pandas, Numpy
<h2>Data</h2>
The dataset, from Kaggle, is a combination of historical data and a wide variety of features. We got two datasets (Train.csv and Store.csv) and a test data set (test.csv) that we must predict sales.
Each dataset contains historical sales data for 11,115 Rossmann stores, over a period from January 1, 2013 to July 31, 2015, with close to 1,017,209 observations, categorizing this problem in the "Time Series Forcasting" class, a very important class and delicate in the field of Machine Learning.
<br>
<a target="_blank" href="https://www.kaggle.com/c/rossmann-store-sales/data">Lien vers les données</a>


<h1>Data Analysis</h1>
<h2>Correlation Matrix</h2>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/corr.jpg"  width="70%" title="hover text">
</p>
<p> 
The correlation matrix above shows the correlation between the different features of the training data.
As we can see, sales are strongly influenced by current promotions, weekdays and holidays, as well as by the obvious correlation between sales and the number of customers.
</p>

<h2>Relationship between Promo and Sales</h2>
<p>
The graph below shows the average sales (in all stores) on days with or without promotions.
The effect of the promotion on sales is clearly evident, the promotion having a strongly positive effect on it.
</p>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/Page-12-Image-5.jpg"  title="hover text">
</p>


<h2>Customers is a very important information</h2>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/Page-12-Image-6.jpg"  title="hover text">
</p>
<p> 
The graph above shows the relationship between sales and customers. We notice that sales and customers are highly correlated.
</p>


<h1>Features Selection</h1>
<p>
Data analysis is often not enough to choose the variables to use for predictions. Data-Scientists and statisticians have opted for other additional methods to ensure the quality of the dependent variables and leave only the most significant variables to predict the dependent variable. The simplest and most effective method is Backward-elimination:
<br>
1. Set a threshold of significance to stay in the model (here 0.01).
<br>
2. Build the model with all possible variables.
<br>
3. Take the predictor that has the greatest p-value if p-value> threshold go to 4 otherwise go to 5.
<br>
4. Remove the predictor, recreate the model without the predictor, recalculate the p-values back to 3.
<br>
5. The model is Ready.
<br>
This algorithm validated the following variables:
 <br><br>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/pval.PNG" title="hover text">
</p>
</p>

<h1>Learning</h1>
<h2>Neural Networks</h2>
<h2>LSTM</h2>
<p>
It is a recurrent neural network, very effective in solving the most difficult problems. Indeed, this type of neural networks has the capacity to predict multiple outputs at the same time. In addition, its architecture allows it
to use the outputs relating to past moments in the prediction of the outputs future moments. This feature makes it very effective for
Forcasting Timeseries issues.
LSTMs are the most popular type of recurrent neural networks
because they brought a simple and effective solution to the problem of "Vanshing
Gradient "which has slowed down the evolution of recurrent neural networks for years.
</p>
<p align="center">
  LSTM
  <br><br>
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/lstm.jpg" width="450" title="hover text">
</p>


<h2>Algorithms</h2>
<h2>K-Nearest Neighbors Regressor</h2>
<p>
The K nearest neighbors is a very simple machine learning algorithm that provides a numerical or categorical target according to a measure of similarity (for example, distance functions) according to a specific value of number of neighbors to consider. A simple implementation of KNN regression is to calculate the average of the digital target of the K nearest neighbors. Another approach uses a weighted average based on the inverse distance of the nearest K neighbors relatives.
</p>
<p align="center">
  KNN
  <br><br>
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/J5r01.png" width="450" title="hover text">
</p>



<h1>Performance</h1> 
<h2>Root Mean Square Percentage Error</h2>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/hey2.PNG"  title="hover text">
</p>
<br>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/hey.PNG"  title="hover text">
</p>

<h2>How to use the code ?</h2>
1. Clone the project and uncompress code.rar
<br>
2. In the Dataset folder you will find the dataset of the project
<br>
3. you find a code.py file to visualize the data and all the steps of the realization of the project.
<h2>Contributions</h2>
<h3>Project realized by: </h3>
- Anes Abdelfatah ABBAD.
<br>
- Amira KETFI.
