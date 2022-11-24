---
description: Data Preparation
---

# LO3

## Learning outcome description

The student can collect data and judge its usefulness for the project. The student can also process this data for later use with the AI.

## Self-assessment

* [x] <mark style="color:red;">Undefined</mark>
* [x] <mark style="color:orange;">Orienting</mark>
* [x] <mark style="color:yellow;">Beginning</mark>
* [x] <mark style="color:green;">Proficient</mark>
* [ ] <mark style="color:green;">Advanced</mark>

## Learning Process

### First Evaluation: Week 4

I started looking into the processes for data preperation by playing with a demo given by Georgiana which can be found [here](https://github.com/CoenBeemer/AI/commit/4f88cc582792aa2257a51edcb2019e0e5fe54a6e). Along with this I started working on preparing some datasets of my own, which was sadly not as successful as I hoped it would be.

#### Self Assessment: Orienting

### Second Evaluation: Week 6

I decided to scrape data from kaggle, to be specific the top 100 most upvoted requests from the "classification" category written in python. I manually compiled a list of links to these notebokos into a csv as well as a shorter version(20 entries) used for faster testing(and less strain on the servers).

This week I successfully gathered data from scraping I did on kaggle. This was done by making a script which pulls the HTML from kaggle and then filters through it to extract data. I've also added an optional download so the workbooks will be downloaded locally.

<figure><img src="../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

The filtering is then done using regex expressions to loop through the html. Some of the data needs hot encoding, such as the tags.&#x20;

<figure><img src="../.gitbook/assets/image (1) (1) (3).png" alt=""><figcaption></figcaption></figure>

All the data is then put into a dataframe for further processing.

<figure><img src="../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Self Assessment: Beginning

### Third Evaluation: Week 11

As described in [LO4 week 12](lo4.md#third-evaluation-week-12) I wanted to train an AI for the group project. to do this, I started by processing the data we got as it was not really suitable for direct use with the AI.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

One of the first problems I encountered, was the wide variety of values in the dataset. Depending on the calibration of the sensors and the skin conditions of the test users, the values could range from 0-2.25 or from 0-12. This is a very huge gap which will completely destroy the AI, which is why I decided to introduce a scaler to normalize all the values between 0 and 1. This makes it a lot easier for the AI to detect a pattern and makes the graphs easier to compare. We also have the problem of having a lot of datasets, which makes it pretty frustrating to test a different dataset because you'd have to manually change the dataset every time. For this I decided to add an option to pick a random dataset every time the code is run to make testing with different datasets a lot easier.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption><p>Added a scaler to keep similar values across different sensors/calibrations. Also a random dataset selection to help with testing models with different datasets</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption><p>A graph of low sensor values</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption><p>A graph of high sensor values caused by a different calibration setting/skin conditions</p></figcaption></figure>

The data sometimes has a lot of noise and some sensor values. For this, I decided to filter them using a rolling mean. As you can see in the graph below, it works pretty well! I tried rolling median as well, but they have about the same effect so I decided on using the mean in the end.

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption><p>Added a rolling mean to smooth out noise and sensor errors</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption><p>A graph of the noisy sensor data(blue) and the data filtered using the rolling mean(orange)</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption><p>A comparison between the rolling median and rolling mean methods of filtering the data</p></figcaption></figure>

Most of these graphs and code blocks can be found in the notebook [here](https://github.com/Inn0/STP1StressVisualisation/blob/main/StressThreshold.ipynb).

#### Self Assessment: Proficient
