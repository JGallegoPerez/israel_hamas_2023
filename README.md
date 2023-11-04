# israel_hamas_2023
In this report, we conduct a methodical examination of public sentiment as expressed in YouTube comments concerning the topic of "Israel", with a specific focus on the period preceding and following the events of the October 2023 Hamas-Israel conflict.

**OUTLINE:**

1. <u> Data Collection:</u>
Our initial phase involves the systematic extraction of YouTube comments using the term "Israel". This data collection spans two critical time frames: prior to and subsequent to October 7, 2023 (the day that Hamas initiated the attacks). For this purpose, we employ the **YouTube API**.

2. <u> Data Preprocessing and Feature Engineering:</u>
In the subsequent phase, we utilize the **Pandas** library to pre-process and transform the collected data. This process includes cleansing and the construction of relevant features to enhance the analytical value of the dataset. The refined data is then meticulously formatted into a **CSV** file, optimizing it for subsequent SQL queries (via Google Cloud **BigQuery**).

3. <u> Exploratory Analysis with SQL:</u>
With the data already in the right format, we transition to Google Cloud BigQuery for an in-depth exploratory analysis. The **SQL** language, facilitated by **BigQuery magic**, serves as our tool for mining insights from the dataset. The culmination of this stage is the synthesis of our findings into a dashboard utilizing **Looker Studio**. This tool not only integrates seamlessly with Google Cloud services but also streamlines the extraction of insights from BigQuery.

4. <u> Sentiment Analysis of Comments:</u>
To explore public sentiment in the comments, we utilize the Natural Language Toolkit (**NLTK**) library for sentiment analysis. This exploration includes both qualitative visualizations, such as **wordclouds**, and a quantitative sentiment assessment.

5. <u> Conclusion:</u> We find obvious differences in the public's attitudes towards the term "Israel" before and after the attack, with what appears to be a major sudden shift from positive to negative sentiment. We will discuss how to interpret the results.

**Disclaimer: we should approach the findings of this exploration with caution. It is critical to avoid hasty generalizations or the formulation of biases based on this singular dataset, the tools we employed and the interpretation we may make of the results.**

## Some figures that illustrate the results

### Quantitative analysis

**Looker Studio** dashboard extracted from **BigQuery (SQL-supported)**, summarizing the quantitative results. Extreme increase in public's interest after 7 October 2023 (day of attack by Hamas), which declines over time; shift in channels that cover the topic of "Israel".

![dashboard](https://github.com/JGallegoPerez/israel_hamas_2023/assets/89183135/967fcab0-c7a7-44c5-a572-b42d258e9aae)

### Qualitative analysis

**Wordclouds** before and after the attack. Before the attack, we observe a more heterogeneous mix of topics. After the attack, the content gears towards war, politics and the conflict between Israel and Hamas. 

*Before the attack on 7-October-2023:*

![wordcloud_before](https://github.com/JGallegoPerez/israel_hamas_2023/assets/89183135/3e4b321e-7f78-47da-a856-d1ea732b0e0a)

*After the attack:*

![wordcload_after](https://github.com/JGallegoPerez/israel_hamas_2023/assets/89183135/ce5326f7-8bd1-418b-bbfe-83ba99ccf8c6)

**Sentiment analysis** results. Major shift in public's sentiment from "extremely positive" to "extremely negative", following the escalation:

![sentiment_chart](https://github.com/JGallegoPerez/israel_hamas_2023/assets/89183135/0a5ed928-fb8d-49b7-8fbd-0b896f90b55a)



## Instructions

Our analysis is extensively facilitated by the use of  **Google Cloud Platform (GCP)** services (therefore, it is also preferable if this notebook is run from Google Colab). Previous experience with GCP is recommended.

Install dependencies from *requirements.txt* 
