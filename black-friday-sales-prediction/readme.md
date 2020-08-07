<h2><a href='https://datahack.analyticsvidhya.com/contest/black-friday'>Analytics Vidhya Hackathon</a></h2>

<p><b>Score Achieved: </b> 2470.81 with rank of 228 out of 2357 active participants as on 7-Aug-2020</p>

<h3>Problem Statement</h3>
<p>A retail company “ABC Private Limited” wants to understand the customer purchase behaviour (specifically, purchase amount) against various products of different categories. They have shared purchase summary of various customers for selected high volume products from last month.
The data set also contains customer demographics (age, gender, marital status, city_type, stay_in_current_city), product details (product_id and product category) and Total purchase_amount from last month.

Now, they want to build a model to predict the purchase amount of customer against various products which will help them to create personalized offer for customers against different products.</p>

<h3>Data</h3>
<table class="table-striped" style="margin-left:20px"><tbody><tr style="height:40px;"><th style="width:150px;height:40px"><b>Variable</b></th><th class="col-md-9">Definition</th></tr><tr style="height:40px;"><td style="width:150px"><b>User_ID</b></td><td class="col-md-9">User ID</td></tr><tr style="height:40px;"><td style="width:150px"><b>Product_ID</b></td><td class="col-md-9">Product ID</td></tr><tr style="height:40px;"><td style="width:150px"><b>Gender</b></td><td class="col-md-9">Sex of User</td></tr><tr style="height:40px;"><td style="width:150px"><b>Age</b></td><td class="col-md-9">Age in bins</td></tr><tr style="height:40px;"><td style="width:150px"><b>Occupation</b></td><td class="col-md-9">Occupation (Masked)</td></tr><tr style="height:40px;"><td style="width:150px"><b>City_Category</b></td><td class="col-md-9">Category of the City (A,B,C)</td></tr><tr style="height:40px;"><td style="width:150px"><b>Stay_In_Current_City_Years</b></td><td class="col-md-9">Number of years stay in current city</td></tr><tr style="height:40px;"><td style="width:150px"><b>Marital_Status</b></td><td class="col-md-9">Marital Status</td></tr><tr style="height:40px;"><td style="width:150px"><b>Product_Category_1</b></td><td class="col-md-9">Product Category (Masked)</td></tr><tr style="height:40px;"><td style="width:150px"><b>Product_Category_2</b></td><td class="col-md-9">Product may belongs to other category also (Masked)</td></tr><tr style="height:40px;"><td style="width:150px"><b>Product_Category_3</b></td><td class="col-md-9">Product may belongs to other category also (Masked)</td></tr><tr style="height:40px;"><td style="width:150px"><b>Purchase</b></td><td class="col-md-9">Purchase Amount (Target Variable)</td></tr></tbody></table>


Your model performance will be evaluated on the basis of your prediction of the purchase amount for the test data (test.csv), which contains similar data-points as train except for their purchase amount. Your submission needs to be in the format as shown in "SampleSubmission.csv".


We at our end, have the actual purchase amount for the test dataset, against which your predictions will be evaluated. Submissions are scored on the root mean squared error (RMSE). RMSE is very common and is a suitable general-purpose error metric.
