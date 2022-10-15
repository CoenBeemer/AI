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
* [ ] <mark style="color:green;">Proficient</mark>
* [ ] <mark style="color:green;">Advanced</mark>

## Learning Process

### First Evaluation: Week 4

I started looking into the processes for data preperation by playing with a demo given by Georgiana which can be found [here](https://github.com/CoenBeemer/AI/commit/4f88cc582792aa2257a51edcb2019e0e5fe54a6e). Along with this I started working on preparing some datasets of my own, which was sadly not as successful as I hoped it would be.

#### Self Assessment: Orienting

### Second Evaluation: Week 6

I decided to scrape data from kaggle, to be specific the top 100 most upvoted requests from the "classification" category written in python. I manually compiled a list of links to these notebokos into a csv as well as a shorter version(20 entries) used for faster testing(and less strain on the servers).

This week I successfully gathered data from scraping I did on kaggle. This was done by making a script which pulls the HTML from kaggle and then filters through it to extract data. I've also added an optional download so the workbooks will be downloaded locally.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

The filtering is then done using regex expressions to loop through the html. Some of the data needs hot encoding, such as the tags.&#x20;

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

All the data is then put into a dataframe for further processing.

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

#### Self Assessment: Beginning
