
## **Introduction**

**What is the focus of the discussion?**
The primary focus is on developing a predictive system utilizing AI technology to forecast the quality of blackberries.

**Why is this focus area important or relevant?**
With the increasing global population and rising demand for fruits and vegetables, particularly commercial crops like blackberries, ensuring top-quality produce becomes crucial. This prediction AI aims to solve the difficulties in maintaining and improving the quality of blackberries while making planning, production processes, and yield optimization more efficient.

**Who is involved or impacted by this focus area?**
 This focus area directly impacts stakeholders involved in blackberry cultivation, including my father, who holds a managerial role within a blackberry farming company that prefers anonymity. While specific company names are withheld for confidentiality reasons, the insights and tools developed within this project are envisioned to benefit not only my father, as a representative stakeholder, but also other blackberry farmers seeking improved quality forecasting methods within the industry.

**When is this focus area significant or relevant?**
This focus area becomes significant in the current context due to the increasing demand for blackberries and the necessity to meet consumer expectations regarding quality. It is particularly relevant in today's era of advancing technology, where AI applications offer innovative solutions for quality assurance.

**How will this prediction AI achieve the intended goals?**
 By harnessing AI technology, this predictive model aims to analyze and predict the quality of blackberries. It will likely utilize data on various parameters like environmental conditions, harvesting methods, fruit characteristics, and other factors influencing blackberry quality to create a predictive model. This model can assist in optimizing planning, production, and yield for commercial blackberry farming.

## **Domain Understanding**

As someone intimately involved in the fruit industry, particularly with blackberries, my domain understanding is not solely derived from external sources or research. Instead, it is grounded in firsthand experience gained through personal work within the industry and insights gleaned from my father, Evert Fieret, who holds a managerial position in a company closely involved with blackberry production and processing.

Quality reigns supreme in the fruit industry, and with blackberries, precision is paramount. The ideal blackberry must avoid being too hard, too soft, or leaking; instead, it must meet exacting standards. Additionally, the demand for blackberries often requires swift and high-volume picking to meet market requirements, a task made challenging due to the fruit's fragility.

## Interview

**Into**
For this interview I am interviewing my father, Evert Fieret. He has a managerial position in the company and knows what goes around. He is mostly in charge of sealing so encounters picking and the good and bad aftermaths of the system they are using.

**Why would it be useful to know the quality and weight the picker is most likely to pick?**
It is useful because then we will be able to plan for it. If we know how much we might have to throw away or save it will be slightly easier to predict how much time picking the fruit will cost and will be able to save allot of time this way.

**How do you see how much you need to pick now?**
Right now we use the system of seeing how many pallets we need to deliver and go a little bit over that. Because of this sometimes we don't have enough and during the sealing of the blackberries we have to go picking again. Sometimes we have to much and if we can't use it we try to sell it ourselves but most of it gets thrown away after some time because it goes bad.

**Are there any other negatives from the way you are picking now?**
At this moment, if we have a big order and we aren't sure if we can pick it ourselves, we need to order it somewhere else. It has happened before that we did order it somewhere but eventually didn't need it. Because of this allot of blackberries have been thrown away and that is a big loss of money and a giant waste.

**Are there any good parts about the way you are picking now?**

Because we have been using this way of picking for a very long time, we have become better at doing it like this. So instead of having to check anywhere or do any calculations some of us know how much we need to pick or if we need to order extra. It has really become a fast way of working and doesn't cost allot of time. It is just that it is not the most efficient way.

Now that we have a little bit of background and knowledge, lets look into the details. I have set up a couple of questions to answer to give myself more of a guideline. These questions can be seen below.

**1. What are the most important variables that have impact on the quality and the weight of a picked blackberry?**

Some of the most important variables to determine the quality of a blackberry are the size, the damage, the taste, the color, and its firmness.

**2. How can these variables be measures?**

These variables are measured every time they are picked. They are weighed, tasted and are visually graded by experts. This process can be automated via visual recognition.

**3. Are there any external factors that can influence the quality?**

Yes, there are. Such as the person who picked the blackberry, if they handled the fruit right. Another thing is it could be picked from different locations and plots like a greenhouse or outside? If it was from the outside, the weather and season could have a very big influence. The time of which it was picked and checked could also make a big difference.

## Conclusion

Accurate predictions of quality and weight can provide a solid foundation for planning. By knowing in advance how much fruit may need to be discarded due to subpar quality or how much needs to be ordered extra, the process of picking and delivery can be made more efficient. This foresight can be used for more efficient resource allocation and cost management.

The current system, which relies on estimating the number of pallets needed, often leads to imprecise outcomes. This can result in costly consequences, such as having to pick more blackberries last minute or facing the dilemma of what to do with excess produce. Predicting quality and weight reduces these risks, enabling better-informed decision-making.

My conclusion, a data-driven approach to quality and weight estimation can significantly reduce waste and financial losses.

#
# **Data Sourcing**

The dataset is I am using if actual data from a blackberry farmer my father works for. I am allowed to use this data, but they asked me to not name them so I will respect that. They provided me with their latest picking data of the whole month of august, which is has a total of 6067 rows. The data this model has is mostly focused on the outside influence of a blackberry instead of things like color or size. The original data provided includes the data and time, the Workers Id numbers, their names (which have been removed due to privacy), the locations where the blackberries were picked, in what crate they were picked, the number of crates scanned, the rate per unit, the quality they were rated at and the weight of the crates when they were scanned.

The time data I have received is not from the time the blackberries were picked but when the crates were scanned. Because of this I chose to categorize the date instead of the exact moments to before or after a break. This will create the most accurate embodiment of time. The breaks are: 10:00 AM to 10:15 AM, 12:00 PM to 12:30 PM and 3:00 PM to 3:15PM.

Both the number of crates scanned and the rate per unit columns are removed because the number of crates scanned is always 1 and the rate per unit has allot of empty values and since it doesn't give any value to me at this moment.

![](RackMultipart20240104-1-pwrcew_html_be70503c58b76a41.png)

The features "Eenheden", "Netto gewicht" and "Bruto gewicht" all come down to the same value so that is why the correlation of those always are quite close to each other. As for all the other Features, there is not much correlation to see. I don't agree with that statement.

For Quality I chose for the Location, Time, Worker number and Fust. I went for these features even though Fust is the only one that shows any correlation with quality. I went for this because i used to work at the company I got the data from and know that these features have no effect the quality.

Every Location grows the blackberries differently so they can test which gives the best quality and which one gives the most blackberries. The time matters allot for the attention of the person. Some people have more attention in the morning and some more in the evening. Also, the weather could have a big impact and if it is a hot day and they are too long in the hot temperature it can damage the blackberry and bring down the quality. Each person picks the blackberries in their own way. Some are more careful than others which is why worker number is in there too.

## **Requirements**

| **Requirement** | **Data Type** | **Units** | **Range** |
| --- | --- | --- | --- |
| **Date** | Date | Date | - |
| **Time** | Categorical | - | 0 -> 1 -> 2 -> 3 |
| **Worker Number** | Numerical | ID's | - |
| **Location** | Categorical | - | 1 -> 2 -> 8 -> 9 |
| **Fust** | Categorical | - | AH 1 x CBL-8 -. AH 4 x CBL-8 -\> Klasse 2 ( 12 x 150 gr ) |
| **Firmness** | Categorical | - | 1 -> 2 -> 3 -> 4 -> 5 |
| **Flavor** | Categorical | - | 1 -> 2 -> 3 -> 4 -> 5 |
| **State** | Categorical | - | 1 -> 2 -> 3 -> 4 -> 5 |
| **Quality** | Categorical | - | Uitstekend -\> Goed -\> Gemiddeld -\> Matig |
| **Weather Conditions** | Categorical | - | Sunny -\> Cloudy -\> Rainy -\> Snowy -\> etc. |
| **Temperature** | Numerical | Celsius | -25°C to 50°C |
| **Soil** | Categorical | - | Potted -\> Wet -\> Fed -\> etc. |
| **Lighting** | Categorical | - | LED -\> Sun -\> None -\> etc. |
| **Plant Condition** | - | - | Fresh or Frozen |


## **Analytic Approach**

The primary objective of this analysis is to predict blackberry quality by leveraging machine learning models and exploratory analysis. The target variable of interest here is 'blackberry quality,' which will be classified based on various features, including worker number, location, time, and fust (potentially related to packaging or container information)

**Model Selection and Justification**

Given the significance of predicting blackberry quality for optimal planning and yield, the models chosen for this predictive analysis are Decision Tree, KMeans Clustering, and Random Forest. These models have demonstrated effectiveness in classification tasks and are suitable for handling categorical and numerical data, making them pertinent for this scenario. The decision to employ these models was based on their interpretability (Decision Tree), clustering capabilities (KMeans), and ensemble learning effectiveness (Random Forest) in classifying blackberry quality based on various features.

**Feature Engineering and Preprocessing**

The provided dataset was subjected to preprocessing steps to refine the data for model training and analysis. Features like "Eenheden," "Netto gewicht," and "Bruto gewicht," which were closely related, were appropriately handled to avoid redundancy and overfitting. Additionally, categorization of the date based on specific breaks instead of exact timestamps was employed to capture optimal time intervals for analysis. Features such as Worker Number, Location, Time, and Fust were selected as they were observed to potentially influence blackberry quality, despite limited correlations in the initial assessment.

**Model Evaluation and Performance Metrics**

The models were evaluated based on crucial performance metrics: accuracy, precision, recall, and F1-score. Nearest Neighbor served as a baseline model, providing initial insights into classification performance. The Decision Tree model demonstrated an accuracy of 81.3% with precision, recall, and F1-score averaging at 76.9%, 65.97%, and 64.34% respectively. The Random Forest model showed improved accuracy at 82.29% with precision, recall, and F1-score averaging at 78.96%, 69.27%, and 70.27% respectively. KMeans Clustering was assessed using the Silhouette Score, achieving a value of 0.6981634187130692, indicating a reasonable clustering performance.

**Further Analysis and Future Steps**

Moving forward, additional exploratory analysis will be conducted to delve deeper into the impact of weather conditions, temperature, soil, and lighting on blackberry quality. Incorporating these factors into the predictive models might enhance their accuracy and provide a more comprehensive understanding of quality determinants.

**Validation and Deployment**

The models will undergo further validation using cross-validation techniques to ensure robustness and generalizability. Following validation, the most effective model will be selected for deployment to aid in real-time quality prediction during blackberry picking. This deployment aims to provide practical assistance in planning, resource allocation, and waste reduction strategies for the agricultural company.


## Delivery Phase

# Introduction

Welcome to the Demonstration and Delivery Phase of my blackberry quality prediction project! This document is dedicated to showcasing the live demonstration of the machine learning model via an HTML front end, highlighting user interaction and stakeholder feedback.

The primary objective of this document is to present a hands-on display of the machine learning model's functionality through the user interface. This demonstration enables my stakeholder, my father, who holds a managerial role at the blackberry farm, to actively engage with the system and provide invaluable feedback.

Throughout this phase, emphasis will be placed on displaying the inputs available within the HTML front end, illustrating the variety of user interactions and the subsequent results generated by the machine learning model. Additionally, the stakeholder's feedback, derived from their experience with the system, will be detailed and analyzed.

# Machine Learning Project Overview

## Objectives

The primary aim of this machine learning project is to predict the quality of blackberries for enhanced planning and production processes at a blackberry farm. By harnessing predictive analytics, the goal is to assist the farm in anticipating blackberry quality, thereby facilitating smarter planning decisions and optimizing harvest yield.

## Methodology and Technologies Utilized

The core methodology employed in this project centers on the implementation of a Random Forest model, a robust ensemble learning technique known for its predictive accuracy and ability to handle large datasets.

## Random Forest Model:

A Random Forest model operates by constructing multiple decision trees during the training phase and outputting the average prediction of individual trees. It excels in handling high-dimensional data and provides insights into feature importance, making it an ideal choice for this predictive endeavor.

Illustration of Random Forest Model:

![](RackMultipart20240104-1-sf1fjy_html_4ad968ea46936d55.png)

## Feature Selection

Key features selected for predictive modeling include:

- Locatie: Captures the geographical location of blackberry cultivation.
- Tijd: Represents the time-related factors impacting blackberry quality.
- Werknemer nr.: Reflects the employee ID contributing to the production process.

- Fust: Selected based on correlation analysis using a heatmap, indicating a significant relationship with blackberry quality.

## Feature Selection Rationale

The selection of "Fust" was substantiated by a correlation heatmap, which highlighted its strong correlation with blackberry quality. The inclusion of "Locatie," "Tijd," and "Werknemer nr." stemmed from experiential insights into their potential impact on blackberry quality, drawing from previous agricultural expertise.

This method mixed real-world observations with data-driven information to help pick the most important features needed to build a strong predictive model.

Correlation heatmap:

![](RackMultipart20240104-1-sf1fjy_html_be70503c58b76a41.png)

# Demonstration of HTML Front End

## Input options

1. Locatie Dropdown
  - Type: Dropdown menu.
  - Purpose: Allows users to select a specific location from a list of options.
  - Options:
    - "01 - Kas Afd"
    - "02 - Kas Afd"
    - "08 - Buitenteelt achter kas Afd"
    - "09 - Buitenteelt Naast kas Afd"
2. Tijd Dropdown
  - Type: Dropdown menu.
  - Purpose: Offers users categorized time periods for selection.
  - Options:
    - "Before 10:00 AM"
    - "Between 10:15 AM - 12:00 PM"
    - "Between 12:30 PM - 3:00 PM"
    - "After 3:15 PM"
3. Werknemer nr. Text Field
  - Type: Text input field.
  - Purpose: Allows users to input a specific numerical identifier or code associated with a worker/employee number.
4. Fust Dropdown
  - Type: Dropdown menu.
  - Purpose: Offers types of fusts for selection.
  - Options:
    - "AH 1 x CBL-8"
    - "AH 4 x CBL-8"
    - "Klasse 2 (12 x 150 gr)"

![](RackMultipart20240104-1-sf1fjy_html_adc92977f5d1e8b1.png)

# Stakeholder Interaction and Feedback

## Stakeholder Engagement

During the live demonstration, the stakeholder interacted with the HTML front end, providing inputs for the predictive model based on their insights and experience within the farming domain.

Inputs Provided by the Stakeholder:

![](RackMultipart20240104-1-sf1fjy_html_eb33e8ccf3e4372.png)

He chose the worker number 20 because that is his own number. He says this are his most frequent occurrences when picking since he doesn't do that to often.

Result:

![](RackMultipart20240104-1-sf1fjy_html_7359537f6420cb58.png)

## Feedback Received

#### **Positive Aspects:**

**Consistent Color Scheme:** The stakeholder appreciated the system's color scheme, which resembled their existing setup. This consistency eased navigation and familiarity.

**Dropdown Functionality:** The dropdown feature was commended for its clarity and ease of use, reducing errors in data entry.

#### **Areas for Improvement:**

**Scale Consideration:** The stakeholder noted that the current system might not immediately cater to their farm's scale, particularly in predicting for a larger number of individuals. They implied that the current version might be more beneficial at a grander scale, suggesting potential utility when managing a higher volume of data or individuals.

**Utility Evaluation:** Although acknowledging the promising start, the stakeholder conveyed that the current iteration isn't significantly useful for their immediate needs. They stressed the inclusion of weight-related metrics to enhance practicality and utility for farm planning purposes.

#### **Additional Features or Modifications Requested:**

**Incorporation of Weight Metrics:** Highlighting its importance, the stakeholder emphasized the need to include weight-related metrics in the system. This addition is seen as crucial for effective planning.

**Consideration for Scale Expansion:** Expressing interest in the system's potential scalability, the stakeholder suggested that while the current version may not fully meet their needs, it might become more valuable when predicting for a larger number of individuals.

# Conclusion

My demonstration phase marked an important step in showcasing my predictive model and gathering valuable feedback. While this phase concludes my current efforts, it lays the groundwork for potential future enhancements.

**Recognizing Positives:**
 The positive response to the system's familiarity in design and the user-friendly dropdowns highlights their importance for potential future iterations. These elements, well-received by stakeholders, serve as strong foundations for continued development.

**Addressing Improvement Opportunities:**
 Stakeholders noted potential limitations in handling larger datasets and stressed the necessity of incorporating weight-related metrics. Though my immediate efforts conclude here, this feedback guides the roadmap for potential future iterations, aiming for enhanced scalability and data inclusivity.

**Vision for Continuity and Development:**
 While my current phase draws to a close, the insights gained provide a vision for the project's future trajectory. Envisaging a more refined and adaptable model, should the project continue, aligns with my long-term goal of creating a solution that evolves with the farm's changing needs.

**Project's Future Path:**
 While this phase concludes my immediate efforts, the gathered insights form a blueprint for potential future developments. Continuing the project's trajectory would involve iterative improvements, focusing on scalability and incorporating weight-related metrics for a more comprehensive predictive model.

**Final Reflections and Prospects:**
 In summary, while this phase marks a milestone, it also sets the stage for potential future advancements. The stakeholder feedback and acquired insights serve as guiding principles, steering my efforts towards a more refined and adaptable solution, should the project pursue further development.
