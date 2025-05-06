<h1 id="air-quality-index-prediction">Air Quality Index (AQI) Prediction</h1>

**Demo: **
<br>
<p>Webapp to predict the Air Quality Index of Mumbai region given climate conditions.</p>

<!--
<p>Environment setup:</p>
<p>requirements.txt: needed only for deployment to Heroku (not needed for local) as there were issues with anaconda installation on it.<br />requirements-conda.txt: needed for local development as I used conda locally. Run: conda create --name <env_name> --file requirements-conda.txt</p> -->


<ol style="list-style-type: decimal">
<li><strong>Data Collection</strong>:<br />For this step, I have written a web scrapper that scraps https://en.tutiempo.net/ for climate data from 2013 to 2018 and creates a HTML file for each month.</li><br>
<li><strong>Data Preprocessing</strong>:<br />For this step, I have taken the data from Krish Naik's project as it was from a paid API.<br />Reference: https://github.com/krishnaik06/AQI-Project/tree/master/Data/AQI.<br />This data contained hourly measurements of AQI.<br />This was converted into a dictionary format where the dictionary key is the year and values are the daily AQI values.<br />Next, the data in step 1 was combined with data of this step to create a new CSV file.</li><br>
<li><strong>Data Cleaning</strong>: <br />The CSV file created in step 2 was cleaned to remove null values and improper data. A new resultant CSV file was created.</li><br>
<li><strong>Feature Engineering and Model Creation</strong>: <br />Tried various algorithms, like Linear Regression, Lasso and Ridge Regression, Decision Tree Regressor, Random Forest Regressor, XGBoost Regressor.<br />Random Forest and XGBoost gave best performance. <b>Finally, used Random Forest Regressor to perform predictions.</b></li>(execute individual jupyter notebooks)<br><br>
<li><strong>Model Deployment</strong>: (execute flask-app in project root, run the app.py file and hit http://127.0.0.1:5000/)<br />Used HTML-CSS frontend to make API calls to Flask REST API backend.<br />Finally deployed on Heroku platform.</li>
</ol>
<p>You can enter various climate details. Finally, click submit button and get your results for Air Quality Index.</p>
**Demo: **
