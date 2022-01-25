# Heart Disease Detection

This Machine Learning webapp was developed to predict if the user, on the basis of input medical parameters is suffering from heart disease or not. Various medical parameters related to the user are taken as input as used to predict the disease. The dataset is taken from Kaggle and app is built using flask.

# Dataset and Input Parameters

The description of the input parameters are given below.

**age** - age in years

**sex** - (1 = male; 0 = female)

**cp** - chest pain type

0: Typical angina: chest pain related decrease blood supply to the heart 
1: Atypical angina: chest pain not related to heart 
2: Non-anginal pain: typically esophageal spasms (non heart related) 
3: Asymptomatic: chest pain not showing signs of disease

**trestbps** - resting blood pressure (in mm Hg on admission to the hospital) anything above 130-140 is typically cause for concern

**chol** - serum cholestoral in mg/dl 
-serum = LDL + HDL + .2 * triglycerides
-above 200 is cause for concern

**fbs** - (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false)
'>126' mg/dL signals diabetes

**restecg** - resting electrocardiographic results 
0: Nothing to note 
1: ST-T Wave abnormality can range from mild symptoms to severe problems signals non-normal heart beat 
2: Possible or definite left ventricular hypertrophy Enlarged heart's main pumping chamber

**thalach** - maximum heart rate achieved

**exang** - exercise induced angina (1 = yes; 0 = no)

**oldpeak** - ST depression induced by exercise relative to rest looks at stress of heart during excercise unhealthy heart will stress more

**slope** - the slope of the peak exercise ST segment
0: Upsloping: better heart rate with excercise (uncommon)
1: Flatsloping: minimal change (typical healthy heart)
2: Downslopins: signs of unhealthy heart

**ca** - number of major vessels (0-3) colored by flourosopycolored vessel means the doctor can see the blood passing through the more blood movement the better (no clots)

**thal** - thalium stress result
1,3: normal
6: fixed defect: used to be defect but ok now
7: reversable defect: no proper blood movement when excercising

**target** - have disease or not (1=yes, 0=no) (= the predicted attribute)

# Development and Deployment

The dataset was imported and features of the dataset was observed. The dataset was checked for nulls and other invalid data.
Pre processing techniques were applied on the data and different visualisations techniques were applied to see the relation of the data and infer what are  the patients health parameters who suffer  from heart disease and other observations. Then we also clean the data and remove outliers. Then once the data is ready we take the model building part. We apply the process of Cross validation where multiple algorithms are used and their cv score is used to determine the algorithm . We have chosen Logistic Regression for our model and after tuning the parameters and then use various parameters to check the performance of the model. Then we dump it into a pickle file.

Flask API is used as for frontend processing and here the pickle file is used to predict if the patient is suffereing from heart disease. Then after that we output the result if the user has heart disease or not.

![kisspng-flask-python-web-framework-bottle-microframework-django-5b3d0ba62504c0 3512153115307273341516](https://user-images.githubusercontent.com/76935226/148778829-022b8b36-35a6-4f76-b609-73a8c2321541.jpg)
![image](https://user-images.githubusercontent.com/76935226/140600298-11b355f2-f0f1-453a-a860-a984817597b5.png)



![Screenshot (168)](https://user-images.githubusercontent.com/76935226/148761790-ca531058-7ecf-470c-a47c-736d54b59ca7.png)
![Screenshot (169)](https://user-images.githubusercontent.com/76935226/148761805-fbb0e266-f196-41e0-b6fd-c06978f8b068.png)
![Screenshot (170)](https://user-images.githubusercontent.com/76935226/148761986-59cdd8a5-91b9-43b8-a99a-9f1bcee47c27.png)
