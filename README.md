# Snowflake Hackathon - Employment Theme

## Project Overview
This project aims to analyze employment data in India using Snowflake and build a Streamlit application that provides insights to bridge skill gaps, enhance job opportunities, and empower individuals towards sustainable employment.

## Features
- **Employment Data Analysis**: Analyzing MGNREGA, National Career Service, PMEGP Scheme data.
- **Sustainability and Inclusivity**: Identifying job opportunities in green sectors and marginalized groups.
- **Mental Health and Employment**: Insights on corporate mental well-being and work-life balance.

## Data Sources
- **MGNREGA (2013-2017)**: Employment under Mahatma Gandhi National Rural Employment Guarantee Act.
- **PMEGP Scheme (2015-2018)**: Job opportunities under the Prime Minister's Employment Generation Programme.
- **Economic Survey 2022-23**: Insights on salary, earnings, and expenditure in India.
- [Open Government Data Platform India](https://data.gov.in/)

## Tech Stack
- **Backend**: Snowflake (for data storage, analysis, and transformation)
- **Frontend**: Streamlit (for building interactive web applications)
- **Version Control**: Git & GitHub
- **Visualization**: Plotly, Pandas
- **Data Wrangling**: Python, SQL

## System Architecture

```mermaid
flowchart TD
    User --> |Interacts with| UI[Streamlit Web App]
    UI --> |Sends request| QAModel[Llama 3.1 Q&A Model]
    UI --> |Sends query| API[API Gateway]
    API --> |Fetches data| DB[Snowflake Database]
    DB --> |Returns data| API
    API --> |Sends data| QAModel
    QAModel --> |Processes and sends response| UI
    UI --> |Displays answer| User

