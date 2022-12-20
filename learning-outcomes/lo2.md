---
description: Investigative Problem Solving
---

# ✔ LO2

## Learning outcome description

The student is able to find problems in a project and can research ways to solve those.



## Self-assessment

* [x] <mark style="color:red;">Undefined</mark>
* [x] <mark style="color:orange;">Orienting</mark>
* [x] <mark style="color:yellow;">Beginning</mark>
* [x] <mark style="color:green;">Proficient</mark>
* [ ] <mark style="color:green;">Advanced</mark>

## Learning Process

### First Evaluation: Week 4

This week I started reading up on model selection and hyperparameter tuning for my personal project, as this was advised to me by Georgiana. I eventually decided to start playing around with [this tutorial](https://www.kaggle.com/code/jhskaggle/l09-model-selection-and-hyperparameter) from kaggle, which can be found [here](https://github.com/CoenBeemer/AI/commit/48f0454c0f0879a0006b39099ac4c64ce9e20bba). I also started looking at the processes for data preperation by looking at a demo also given by Georgiana which can be found [here](https://github.com/CoenBeemer/AI/commit/4f88cc582792aa2257a51edcb2019e0e5fe54a6e).

#### Self Assessment: Orienting

### Second Evaluation: Week 10

While working on a small personal project, I ran into some weird problems in my code. After looking into this with Kazimier and Coen, I figured out the reason for that problem. What I was trying to do was predicting the review rating IGN would give a video game based on its properties such as the genre, publisher and age rating. The anomaly in my code was a very high accuracy (90%) when using randomForest and a very low accuracy(10%) when using a decisionTree. To find the cause of this, we made some visualisations as you can see [here](https://github.com/CoenBeemer/AI/blob/v2/src/ai.ipynb). At a first glance the data didn't seem to show any correlation that the models could pick up on, so I started explaining my code step by step which led to the source of the problem: I accidentally used the training dataset for the randomForest accuracy testing. Eventually the additional data visualisation did help out, because Georgiana later recommended me to use a correlation matrix instead of a scatter plot which gave me a better overview of what data I was actually using.

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

#### Self Assessment: Beginning

### Third Evaluation: week 16

As described in [LO4 week 13](lo4.md#fourth-evaluation-week-13) I have explored [this tutorial](https://www.digitalocean.com/community/tutorials/a-guide-to-time-series-forecasting-with-arima-in-python-3) for use with our group project. I have also written several research documents as described in [LO6 week 16](lo6.md#third-evaluation-week-16). With these documents, I believe I have shown enough investigative problem solving to show this learning outcome at a proficient level.

#### Self Assessment: Proficient
