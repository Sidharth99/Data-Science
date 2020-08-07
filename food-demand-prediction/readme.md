<h2><a href='https://datahack.analyticsvidhya.com/contest/genpact-machine-learning-hackathon-1/#LeaderBoard'>Analytics Vidhya Hackathon</a></h2>

<p><b>Score Achieved :</b> 56.28 with rank 339 out of 1393 active participants and 10836 registrations as on 7-Aug-2020 [model: RandomForestRegressor]</p>

<h3>Problem Statement</h3>
Your client is a meal delivery company which operates in multiple cities. They have various fulfillment centers in these cities for dispatching meal orders to their customers. The client wants you to help these centers with demand forecasting for upcoming weeks so that these centers will plan the stock of raw materials accordingly.

The replenishment of majority of raw materials is done on weekly basis and since the raw material is perishable, the procurement planning is of utmost importance. Secondly, staffing of the centers is also one area wherein accurate demand forecasts are really helpful. Given the following information, the task is to predict the demand for the next 10 weeks (Weeks: 146-155) for the center-meal combinations in the test set:  
* Historical data of demand for a product-center combination (Weeks: 1 to 145)
* Product(Meal) features such as category, sub-category, current price and discount
* Information for fulfillment center like center area, city information etc.

<h3>Data Dictionary</h3>
1. Weekly Demand data (train.csv): Contains the historical demand data for all centers, test.csv contains all the following features except the target variable<table style="margin-left: auto; margin-right: auto;" border="1" width="0" cellspacing="5" cellpadding="10">
<tbody>
<tr>
<td><strong>Variable</strong></td>
<td><strong>Definition</strong></td>
</tr>
<tr>
<td>id</td>
<td>Unique ID</td>
</tr>
<tr>
<td>week</td>
<td>Week No</td>
</tr>
<tr>
<td>center_id</td>
<td>Unique ID for fulfillment center</td>
</tr>
<tr>
<td>meal_id</td>
<td>Unique ID for Meal</td>
</tr>
<tr>
<td>checkout_price</td>
<td>Final price including discount, taxes &amp; delivery charges</td>
</tr>
<tr>
<td>base_price</td>
<td>Base price of the meal</td>
</tr>
<tr>
<td>emailer_for_promotion</td>
<td>Emailer sent for promotion of meal</td>
</tr>
<tr>
<td>homepage_featured</td>
<td>Meal featured at homepage</td>
</tr>
<tr>
<td>num_orders</td>
<td>(Target) Orders Count</td>
</tr>
</tbody>
</table>
2. fulfilment_center_info.csv: Contains information for each fulfilment center<table style="margin-left: auto; margin-right: auto;" border="1" width="272" cellspacing="5" cellpadding="10">
<tbody>
<tr>
<td width="81"><strong>Variable</strong></td>
<td width="191"><strong>Definition</strong></td>
</tr>
<tr>
<td>center_id</td>
<td>Unique ID for fulfillment center</td>
</tr>
<tr>
<td>city_code</td>
<td>Unique code for city</td>
</tr>
<tr>
<td>region_code</td>
<td>Unique code for region</td>
</tr>
<tr>
<td>center_type</td>
<td>Anonymized center type</td>
</tr>
<tr>
<td>op_area</td>
<td>Area of operation (in km^2)</td>
</tr>
</tbody>
</table>
3. meal_info.csv: Contains information for each meal being served<table style="margin-left: auto; margin-right: auto;" border="1" width="324" cellspacing="5" cellpadding="10">
<tbody>
<tr>
<td width="59"><strong>Variable</strong></td>
<td width="265"><strong>Definition</strong></td>
</tr>
<tr>
<td>meal_id</td>
<td>Unique ID for the meal</td>
</tr>
<tr>
<td>category</td>
<td>Type of meal (beverages/snacks/soups….)</td>
</tr>
<tr>
<td>cuisine</td>
<td>Meal cuisine (Indian/Italian/…)</td>
</tr>
</tbody>
</table>

<h3>Evaluation Metric</h3>
The evaluation metric for this competition is 100*RMSLE where RMSLE is Root of Mean Squared Logarithmic Error across all entries in the test set.
