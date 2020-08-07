<h2><a href='https://datahack.analyticsvidhya.com/contest/janatahack-demand-forecasting/#ProblemStatement'>JanataHack: Demand Forecasting</a></h2>

<p><b>Score Achieved: </b>475.51 on private LB with rank 73 out of 262 active participants. [model: random forest regressor]</p>

<h3>Problem Statement</h3>
One of the largest retail chains in the world wants to use their vast data source to build an efficient forecasting model to predict the sales for each SKU in its portfolio at its 76 different stores using historical sales data for the past 3 years on a week-on-week basis. Sales and promotional information is also available for each week - product and store wise. 

However, no other information regarding stores and products are available. Can you still forecast accurately the sales values for every such product/SKU-store combination for the next 12 weeks accurately? If yes, then dive right in!

<h3>Data Description</h3>
<table border="1" style="height: 713px;" width="696">
    <tbody>
        <tr>
            <td width="236">
                <p><strong>Variable</strong></p>
            </td>
            <td width="531">
                <p><strong>Definition</strong></p>
            </td>
        </tr>
        <tr>
            <td width="236">
                <p>record_ID</p>
            </td>
            <td width="531">
                <p>Unique ID for each week store sku combination</p>
            </td>
        </tr>
        <tr>
            <td width="236">
                <p>week</p>
            </td>
            <td width="531">
                <p>Starting Date of the week</p>
            </td>
        </tr>
        <tr>
            <td width="236">
                <p>store_id</p>
            </td>
            <td width="531">
                <p>Unique ID for each store (no numerical order to be assumed)</p>
            </td>
        </tr>
        <tr>
            <td width="236">
                <p>sku_id</p>
            </td>
            <td width="531">
                <p>Unique ID for each product <span style="color: rgb(0, 0, 0); font-family: Times; font-size: medium; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; text-decoration-style: initial; text-decoration-color: initial; display: inline !important; float: none;">(no numerical order to be assumed)</span></p>
            </td>
        </tr>
        <tr>
            <td width="236">
                <p>total_price</p>
            </td>
            <td width="531">
                <p>Sales Price of the product&nbsp;</p>
            </td>
        </tr>
        <tr>
            <td width="236">
                <p>base_price</p>
            </td>
            <td width="531">
                <p>Base price of the product</p>
            </td>
        </tr>
        <tr>
            <td width="236">
                <p>is_featured_sku</p>
            </td>
            <td width="531">
                <p>Was part of the featured item of the week</p>
            </td>
        </tr>
        <tr>
            <td width="236">
                <p>is_display_sku</p>
            </td>
            <td width="531">
                <p>Product was on display at a prominent place at the store</p>
            </td>
        </tr>
        <tr>
            <td width="236">
                <p>units_sold</p>
            </td>
            <td width="531">
                <p>(Target) Total Units sold for that week-store-sku combination</p>
            </td>
        </tr>
    </tbody>
</table>

<h3>sample_submission.csv</h3>
<table border="1" cellpadding="2" cellspacing="2" style="box-sizing: border-box; border-collapse: collapse; color: rgb(74, 74, 74); font-family: Roboto, sans-serif; font-size: 16px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: left; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-style: initial; text-decoration-color: initial; width: 417px;">
    <tbody style="box-sizing: border-box;">
        <tr style="box-sizing: border-box;">
            <td align="left" height="17" style="box-sizing: border-box; width: 174px; text-align: center;"><strong>Variable</strong></td>
            <td align="left" style="box-sizing: border-box; width: 233px; text-align: center;"><strong style="box-sizing: border-box; font-weight: bolder;">Description</strong></td>
        </tr>
        <tr style="box-sizing: border-box;">
            <td align="left" height="17" style="box-sizing: border-box; width: 174px;">
                <p>record_ID</p>
            </td>
            <td align="left" style="box-sizing: border-box; width: 233px; text-align: left; vertical-align: middle;">
                <p>Unique ID for each week store sku combination</p><br>
            </td>
        </tr>
        <tr style="box-sizing: border-box;">
            <td align="left" height="47" style="box-sizing: border-box; width: 174px; vertical-align: middle; text-align: left;">
                <p>units_sold</p><br>
            </td>
            <td align="left" style="box-sizing: border-box; width: 233px; text-align: left;">(Target) Total Units sold for that week-store-sku combination</td>
        </tr>
    </tbody>
</table>

<h3>Evaluation Metric</h3>
The evaluation metric for this competition is 100*RMSLE (Root Mean Squared Log Error).
