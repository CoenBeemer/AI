---
description: Data Visualization
---

# LO5

## Learning outcome description

The student can display the data in a way which is useful and/or interesting to the target group.

## Self-assessment

* [x] <mark style="color:red;">Undefined</mark>
* [x] <mark style="color:orange;">Orienting</mark>
* [x] <mark style="color:yellow;">Beginning</mark>
* [ ] <mark style="color:green;">Proficient</mark>
* [ ] <mark style="color:green;">Advanced</mark>

## Learning Process

### First Evaluation: Week 7

I made several data visualisations for the data gathered from the web scraping. I made several bar graphs and boxplots in an attempt to figure out relations in the data which my AI could use as indicators for certain datatypes. My data is a bit skewed, as my data has been filtered on one of these tags (I think you can guess which one).

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

#### Self Assessment: Orienting



### Third Evaluation: Week 10

As explained in [LO2 week 10](lo2.md#second-evaluation-week-10) I made several visualizations for my personal project to see if there is any correlation in the data. I initially started with making scatter plots such as this one:&#x20;

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption><p>A scatter plot for trying to figure out if the game score is related to release dates somehow</p></figcaption></figure>

However this didn't show much correlation so I tried adding more features like this:&#x20;

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption><p>That same scatter plot but with age rating as added feature</p></figcaption></figure>

This didn't help much either though, which is why Georgiana recommended looking into correlation matrices. This did help somewhat, though not much because I have so many features which causes the resolution to become an issue:

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p>A correlation matrix of almost 2000 features</p></figcaption></figure>

As you can see there are some dots spread around which indicates correlation, but with the sheer amount of features (almost 2000) there is no way of telling what is what. Because of this, I decided to split up the features into smaller blocks(of about 200) which will give a much clearer image of where significant data can be found. This image for example shows a clear hotspot around the resolution features:

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>A correlation matrix of about 200 features with a clear hotspot in the top right</p></figcaption></figure>

#### Self Assessment: Beginning (almost proficient)

### How I will show this learning outcome

I believe I will be able to show this learning outcome at a proficient level by improving my visualisations a bit more by for example showing a time series instead of the unix timestamp  in the graphs. I will do this in my personal project and I will also correct this in the group project where a measurement index is used instead.

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>
