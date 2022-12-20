---
description: Machine Teaching
---

# ✔ LO4

## Learning outcome description

The student is able to train an algorithm/AI by using datasets and can test if the algorithm/AI has been trained (well) enough to serve its purpose.

## Self-assessment

* [x] <mark style="color:red;">Undefined</mark>
* [x] <mark style="color:orange;">Orienting</mark>
* [x] <mark style="color:yellow;">Beginning</mark>
* [x] <mark style="color:green;">Proficient</mark>
* [ ] <mark style="color:green;">Advanced</mark>

## Learning Process

### First Evaluation: Week 4

This week I started looking into a demo given by Georgiana, which includes kNN and decision tree algorithms used for training an AI. you can find what I did in more detail [here](lo3.md#first-evaluation-week-4).

#### Self Assessment: Orienting

### Second Evaluation: Week 10

As explained in [LO2 week 10](lo2.md#second-evaluation-week-10) I started training an AI for predicting scores of IGN reviews based on the features of the game. I did start off with a flop, my data didn't really seem to have any correlation to the result I wanted to predict as you can see in the visuals in [LO3 week 10](lo3.md#third-evaluation-week-10).

#### Self Assessment: Beginning

### Third Evaluation: Week 12

For the group project I wanted to make an AI to detect stress levels. For this I trained an AI on (bad) data from the client, which has a good accuracy without overfitting as it works on multiple datasets without retraining.

<figure><img src="../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>

#### Self Assessment: Beginning



### Fourth Evaluation: Week 13

I processed the feedback given in the previous evaluation by following [this tutorial ](https://www.digitalocean.com/community/tutorials/a-guide-to-time-series-forecasting-with-arima-in-python-3)based around predicting values in a TimeSeries using the ARIMA model. This exploration can be found [here](https://github.com/Inn0/STP1StressVisualisation/blob/arima/StressThreshold.ipynb). To do this, I modified it so I could try if it works on the group project dataset to see if it is relevant for our use case. Because I suspected it would probably not work as our dataset is very different, I mostly looked into the data preparation that was done to see if I could apply this for our own project as well. Somehow, the method I used to process the data is very similar to the way it's done in the tutorial.

My data preprocessing:

`df1_2['RollingMean'] = df1_2['RangeCAL_uS'].rolling(40).mean()`

The tutorial's data preprocessing:

`df_co2 = df_co2['co2'].resample('MS').mean()`

As you can see above, I used a rolling mean as where the tutorial used a resample with the mean. The resample can be used to increase the amount of datapoints while I keep my data size the same. I believe my method will work the best with a live datastream as it runs a lot faster, so I will not change this in our product.

The tutorial notebook also contains a visualisation of the data correlation, which should look similar to this:&#x20;

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption><p>Correlation visualization from the tutorial</p></figcaption></figure>

It is clear that our dataset will not work right away, as it looks like this instead:

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption><p>correlation visualization for our own dataset</p></figcaption></figure>

As you can see in the top right the data does not follow a normal distribution and the plot on the bottom left shows that the ordered distribution of residuals do not closely follow a linear trend. This tells us that this model will not work well with the data, which is visible in the visualization below:

<figure><img src="../.gitbook/assets/image (3) (3).png" alt=""><figcaption><p>Visualization of the dynamic forecast of the model, its likely inaccuracy and the observed data(actual measurements from the dataset)</p></figcaption></figure>

As you can see the prediction does get the general trend of the data, but it does not follow the actual data at all and the inaccuracy is immense. I believe this is because the dataset does not contain a clear periodic pattern which will lead to the AI having to make a shot in the dark.

I believe I've shown this learning outcome to a proficient level as I have trained several models with varying success and explanations on why the model is (not) successful.&#x20;

#### Self Assessment: Proficient
