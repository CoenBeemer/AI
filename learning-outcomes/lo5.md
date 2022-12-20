---
description: Data Visualization
---

# ✔ LO5

## Learning outcome description

The student can display the data in a way which is useful and/or interesting to the target group.

## Self-assessment

* [x] <mark style="color:red;">Undefined</mark>
* [x] <mark style="color:orange;">Orienting</mark>
* [x] <mark style="color:yellow;">Beginning</mark>
* [x] <mark style="color:green;">Proficient</mark>
* [ ] <mark style="color:green;">Advanced</mark>

## Learning Process

### First Evaluation: Week 7

I made several data visualisations for the data gathered from the web scraping. I made several bar graphs and boxplots in an attempt to figure out relations in the data which my AI could use as indicators for certain datatypes. My data is a bit skewed, as my data has been filtered on one of these tags (I think you can guess which one).

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

#### Self Assessment: Orienting



### Third Evaluation: Week 10

As explained in [LO2 week 10](lo2.md#second-evaluation-week-10) I made several visualizations for my personal project to see if there is any correlation in the data. I initially started with making scatter plots such as this one:&#x20;

<figure><img src="../.gitbook/assets/image (14) (1).png" alt=""><figcaption><p>A scatter plot for trying to figure out if the game score is related to release dates somehow</p></figcaption></figure>

However this didn't show much correlation so I tried adding more features like this:&#x20;

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption><p>That same scatter plot but with age rating as added feature</p></figcaption></figure>

This didn't help much either though, which is why Georgiana recommended looking into correlation matrices. This did help somewhat, though not much because I have so many features which causes the resolution to become an issue:

<figure><img src="../.gitbook/assets/image (3) (2).png" alt=""><figcaption><p>A correlation matrix of almost 2000 features</p></figcaption></figure>

As you can see there are some dots spread around which indicates correlation, but with the sheer amount of features (almost 2000) there is no way of telling what is what. Because of this, I decided to split up the features into smaller blocks(of about 200) which will give a much clearer image of where significant data can be found. This image for example shows a clear hotspot around the resolution features:

<figure><img src="../.gitbook/assets/image (1) (3).png" alt=""><figcaption><p>A correlation matrix of about 200 features with a clear hotspot in the top right</p></figcaption></figure>

#### Self Assessment: Beginning (almost proficient)

### Fourth Evaluation: Week 16

As seen in [LO4 week 13](lo4.md#fourth-evaluation-week-13) I have improved my data visualisations by adding on timestamps instead of a measurement index. I've also improved the other visualizations by adding a legend and improving the readability.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption><p>A graph of the sensor values and stress levels over time</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>A visualization of the model's predicted values against the expected values</p></figcaption></figure>

#### Self Assessment: Proficient

###
