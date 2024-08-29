# DNPAO Project
Red Team members' (Firstname's order): _Harrison Lee, Kiet Hoang, Michael MacInnis, Michael Nurthen, Temi Olufemi_

# An overview of the project and its purpose

_Project Aim:_ This project aims to analyze demographic information and its impact on obesity trends in the United States. The dataset was sourced from the BRFSS (Behavioural Risk Factor Surveillance System), which is then used by the CDC's Division of Nutrition, Physical Activity, and Obesity (DNPAO). This dataset contains various demographic information from the United States, which shows how it relates to obesity, exercise and diet habits.

The data used for this project was a large dataset with different categories and questions. We collected and amended it based on the questions, specifically related to diet, exercise, and obesity. The demographic variables include education level, age, ethnicity, gender, and income. These factors are examined to understand their impact on obesity trends. 

The data is stratified by age, education, income, gender, and race, providing detailed insights. Additionally, this dataset includes an "Overall" value for each state, as well as an overall value for the entire nation. We then cleaned it and created a smaller dataset called DNPAO_cleaned.csv, which focuses only on research question "Percent of adults aged 18 years and older who have obesity."

# Instructions on how to use and interact with the project

In the Python script titled "First_Clean.ipynb," we utilized the missingno library, which is an external library that was not covered in our class. This library allowed us to quickly visualize the entire dataset and subsequently clean it up by removing unnecessary columns and ensuring that the new dataset contained no missing data points (NAs).

We have utilized PostGreSQL to store our data (see /Resources/PostGreSQL_queries.sql) and then exported the necessary data in a CSV format for visualization. However, we have decided to use Python (see "Visualizations.ipynb") as an alternative method to further refine and analyze our data for better visualization.

We developed HTML (index.html) and Java scripts (/static/js/ and /static/css) to fulfill the following requirements:

  - HTML menus, dropdowns, and/or textboxes to display JavaScript-powered visualizations

  - Flask backend with interactive API routes that serve back Python or JavaScript created plots

  - Visualizations created from user-selected filtered data

Finally, we have deployed our project to a GitHub page. 

# Visualizations: 
(**focus on a specific year 2022**)

[Fig.1: 3D plot of Percent of Obesity in each Age Group per State]

<img width="979" alt="Screenshot 2024-04-28 at 1 10 37 PM" src="https://github.com/user-attachments/assets/9b8aa195-7af3-4109-9a48-da1000532b87">

[Fig. 2: Percent Obesity Within Each Age Group by State]

<img width="595" alt="Screenshot 2024-04-28 at 1 08 03 PM" src="https://github.com/user-attachments/assets/716a9e26-4f11-4755-a81d-f166f192d2d7">

[Fig.3: National Levels]

The [CDC 2022 Adult Obesity Prevalence Maps](https://www.cdc.gov/obesity/php/data-research/adult-obesity-prevalence-maps.html) for 50 states, the District of Columbia, and 3 U.S. territories show the proportion of adults with a body mass index (BMI) equal to or greater than 30 ( ≥30 kg/m2) based on self-reported weight and height.

![Screenshot 2024-08-28 at 6 37 01 PM](https://github.com/user-attachments/assets/d89c5485-b16a-47f7-baa3-3fe75c4f3b13)
<B> Source:</B> [Behavioral Risk Factor Surveillance System](https://www.cdc.gov/brfss/)

A. By Age

![Screenshot 2024-08-28 at 6 17 27 PM](https://github.com/user-attachments/assets/eb527fd6-1952-46eb-866a-769d22484318)

B. By Education

![Screenshot 2024-08-28 at 6 21 22 PM](https://github.com/user-attachments/assets/b6e4b85f-f121-418d-8a97-3b81fdc71b34)


C. By Income

![Screenshot 2024-08-28 at 6 22 45 PM](https://github.com/user-attachments/assets/30f83ed9-721e-4707-983e-79ec2f2d4f00)

D. By Gender

![Screenshot 2024-08-28 at 6 24 28 PM](https://github.com/user-attachments/assets/15a4b506-c950-4a5d-b74c-6b7817e435b4)

E. By Race/Ethnicity

![Screenshot 2024-08-28 at 6 25 57 PM](https://github.com/user-attachments/assets/66537780-1c93-4d88-ad09-4215e9bf6f23)

F. By the overall total population per state

![Screenshot 2024-08-28 at 6 31 05 PM](https://github.com/user-attachments/assets/6983ceed-fc9f-4611-9e28-d47a88ad012d)

# A paragraph summarizing efforts for ethical considerations made in the project
(_At least one paragraph summarizing efforts for ethical considerations made in the project_)

The way data is usually reported can sometimes make it possible for someone to figure out personal information through reverse engineering. This means that if someone has access to known demographic information about an individual, they could potentially figure out that person's individual responses to a survey, provided that person is specific enough. For instance, if we know that a person is female, aged 18-24, Native American, has a college education, is in the highest income bracket, and lives in Guam in 2022, we could potentially determine their responses to survey questions about their routines, alcohol and tobacco consumption, and other such topics. 

This raises ethical concerns about how the data is reported and served by organizations like the CDC. To address this, the CDC formats the data in a way that only provides information about a specific question along with a specific demographic and group. For example, a document about obesity would contain many records, each one specifying state, year, and age group (e.g. 18-24), but no other demographic information is included in that record. This means that it is not possible to directly relate that data to any specific individual or group.


# References for the data source(s) 

https://dev.socrata.com/foundry/data.cdc.gov/hn4x-zwk7

# References for any code used that is not your own: 
It was a group effort. We wrote the code ourselves, sometimes using AI assistance for debugging and/or optimization.
