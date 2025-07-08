
# Power BI Data Professional Survey Breakdown

This repository contains the files and assets for a guided Power BI project, serving as a final project in a Power BI tutorial series. The project demonstrates a full workflow from **raw data ingestion and transformation** using Power Query to creating **interactive visualizations and dashboards** in Power BI Desktop.

## Project Overview

This project utilises **real-world data** collected through a survey of data professionals on platforms like LinkedIn and Twitter. The survey had approximately **600-700 respondents**. Unlike previous projects that used a fictional dataset, this project provides an authentic experience of working with raw, user-generated data, which often requires significant cleaning and transformation. The goal is to **transform this raw data, create meaningful visualizations, and design a final dashboard** to derive insights into the data professional landscape.

## Data Source

The core of this project is a **CSV file** containing survey responses from data professionals. This raw data was downloaded directly from the survey website and was **not modified in Excel** before being imported into Power BI, ensuring all transformations are performed within Power BI itself. The data file is available for download on GitHub, allowing others to follow along or recreate the project.

## Tools Used

*   **Microsoft Power BI Desktop:**
    *   **Power Query Editor:** Used extensively for **data transformation and cleaning**.
    *   **Power BI Desktop (Report View):** Used for **creating interactive visualizations and designing the final dashboard**.
*   **Microsoft Excel:** Used only for an initial quick review of the raw data; **no data changes were made here**.

## Key Project Steps and Features

The project walkthrough covers several critical steps in the data analysis pipeline within Power BI:

### Data Ingestion and Initial Review

*   The **raw CSV data was imported directly into Power BI's Power Query Editor**.
*   An initial review of the data in Power Query helped identify columns for deletion and areas requiring cleaning based on the desired output.

### Data Transformation and Cleaning (Power Query Editor)

A significant portion of the project focuses on demonstrating practical data cleaning techniques, albeit a simplified set for a beginner tutorial:

*   **Column Removal:** Identified and removed irrelevant columns early in the process to streamline the data.
*   **Standardising Job Titles:**
    *   The "Which title fits you best" column contained numerous free-text "other" entries and variations (e.g., "Software Engineer" vs. "software engineer").
    *   To simplify, the column was **split by a delimiter (open parenthesis)**, and the detailed "other" specifications were discarded. This left a more manageable set of core job titles (e.g., Data Analyst, Data Architect, Engineer, Data Scientist, Database Developer, Other, Student/None).
    *   This approach was taken to avoid extensive data cleaning in Power BI which would typically involve AI or SQL.
*   **Standardising Programming Languages:**
    *   Similar to job titles, the "Favorite programming language" column had pre-selected options and free-text "other" entries with various spellings (e.g., multiple ways people wrote "SQL").
    *   This column was also **split by a colon delimiter**, and the detailed "other" information was discarded to simplify the options presented.
*   **Transforming Yearly Salary Data:**
    *   The "Current yearly salary" was provided as a range (e.g., "106-125k") or with a plus sign (e.g., "225k+") and was initially text.
    *   The column was **duplicated**, then **split by 'digit to non-digit'** to separate the numeric parts.
    *   Symbols like 'K', '-', and '+' were **replaced with blank or specific values** (e.g., '225k+' became '225' for calculation purposes).
    *   The resulting numeric parts were **converted to whole numbers**.
    *   A **new custom column, "Average Salary," was created** by averaging the two numbers from the split range (e.g., (106 + 125) / 2). This provided a usable numeric value for analysis, though it was acknowledged as a simplification and not perfect.
*   **Simplifying Industry and Country Data:**
    *   Due to the large number of unique entries and variations, the "Industry" and "Country" columns were also simplified, often categorising less common entries as 'other' using similar split methods.

### Dashboard Creation and Visualization

The project then moves to creating various visualizations to build a comprehensive dashboard:

*   **Dashboard Title:** A clear title, "**Data Professional Survey Breakdown**," was added.
*   **Cards:** Used to display **high-level summary numbers**, such as the "**Count of Survey Takers**" (630) and "**Average Age of Survey Taker**" (approximately 30 years old). These are meant for quick glances.
*   **Stacked Bar Chart:** Visualises the "**Average Salary by Job Title**". Insights include Data Scientists earning the highest average salary (e.g., £93,000) and Data Analysts making around £55,000 (representing the majority of survey takers). The average salary column's data type was corrected from text to decimal for this visualisation.
*   **Clustered Column Chart:** Displays the "**Favorite Programming Languages**," clearly showing **Python as the most popular**. The chart shows the count of votes for each language.
*   **Tree Map:** Used to break down data by "**Country of Survey Takers**". This enables users to filter by country and observe differences, for example, in average salaries between the United States (Data Scientist: £139,000, Data Analyst: £80,000) and India (Data Scientist: £68,000, Data Analyst: £26,000) due to varying costs of living.
*   **Gauge Charts:** Two gauge charts were created to show "**Happiness with Work-Life Balance**" (average rating ~5.74) and "**Happiness with Salary**" (average rating shown to be lower, highlighting a real-world finding from the survey). These effectively display average ratings on a 0-10 scale.
*   **Pie Chart:** Visualises the "**Average Salary by Gender**," surprisingly showing females with a slightly higher average salary (£55k) compared to males (£53k) in the survey data.
*   **Donut Chart (Difficulty to Break into Data):** Displays the **percentages of responses regarding the difficulty of breaking into data**. Custom colours were applied (red for 'very difficult', orange for 'difficult', yellow for 'neither easy nor difficult', and shades of blue for 'easy' and 'very easy') to enhance readability and insight.
*   **Dashboard Formatting:** Emphasis was placed on organising visualizations, adjusting sizes, and applying a theme to improve the overall aesthetic and user experience. The video demonstrates how to customise themes, including changing specific colours.

## Learning Outcomes

By reviewing or replicating this project, you can gain practical experience in:

*   **End-to-End Power BI Workflow:** From raw data to a finished dashboard.
*   **Working with Real-World Data:** Understanding the complexities and necessary simplifications of raw, unstructured data.
*   **Power Query for Data Transformation:** Key skills in cleaning and shaping data, including splitting columns, replacing values, and creating custom columns.
*   **Creating Diverse Visualizations:** Utilising cards, bar charts, column charts, tree maps, gauge charts, and pie/donut charts to represent different types of data insights effectively.
*   **Dashboard Design Principles:** Organising visualizations and applying themes for improved aesthetics and user interaction.

## Future Improvements and Advanced Work

This project serves as a **beginner-level introduction** to Power BI. The sources highlight that much more extensive data cleaning and advanced visualizations are possible with this dataset. Future enhancements could include:

*   **More Robust Data Standardisation:** Implementing more advanced techniques, potentially using **Excel or SQL** for thorough standardisation of free-text entries (e.g., combining all variations of "SQL" or "Software Engineer").
*   **In-depth Analysis:** Creating more complex analyses and visualizations based on deeper insights from the data.
# 📊 Dashboard & Visualizations

## 📸 Dashboard Preview

![Dashboard Screenshot](https://github.com/Simha-444/powerbi/blob/b211898abe877704dcffe677c658bc9ff5a370c1/final%20Dashboard.png)

