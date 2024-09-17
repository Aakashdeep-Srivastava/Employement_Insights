# Snowflake Hackathon - Employment Theme

## Project Overview
This project aims to analyze employment data in India using Snowflake and build a Streamlit application that provides insights to bridge skill gaps, enhance job opportunities, and empower individuals towards sustainable employment.

## Features
- **Employment Data Analysis**: Analyzing MGNREGA, National Career Service, PMEGP Scheme data.
- **Sustainability and Inclusivity**: Identifying job opportunities in green sectors and marginalized groups.
- **Mental Health and Employment**: Insights on corporate mental well-being and work-life balance.

## Data Sources

The following datasets were used for analyzing and visualizing India's employment landscape:

1. **Ministry of Labour and Employment (India)**
   - **Data Available**: Employment and unemployment trends, job creation statistics, and labor market data.
   - **Source**: [Ministry of Labour and Employment](https://labour.gov.in)
   - **Reports**: Periodic labor surveys, employment reports, and job creation initiatives.

2. **Periodic Labour Force Survey (PLFS) by NSO**
   - **Data Available**: Unemployment rate, labor force participation rate, workforce composition (by gender, sector, etc.).
   - **Source**: National Statistical Office (NSO), Ministry of Statistics and Programme Implementation (MoSPI)
   - **Reports**: PLFS annual and quarterly reports.
   - **Access**: [MOSPI Data](http://mospi.nic.in)

3. **Centre for Monitoring Indian Economy (CMIE)**
   - **Data Available**: Real-time unemployment rate, labor participation, employment in different sectors (urban vs rural).
   - **Source**: [CMIE](https://unemploymentinindia.cmie.com/)
   - **Reports**: CMIE's unemployment tracker and labor market reports.
   - **Access**: Subscription-based access, but some reports are publicly available.

4. **International Labour Organization (ILO) - India**
   - **Data Available**: Labor force data, unemployment figures, gender and age group breakdowns.
   - **Source**: [ILO India](https://www.ilo.org/global/statistics-and-databases/lang--en/index.htm)
   - **Reports**: Employment projections, labor market analysis.

5. **Reserve Bank of India (RBI)**
   - **Data Available**: Economic indicators related to employment, including sectoral growth and unemployment trends.
   - **Source**: [RBI](https://www.rbi.org.in/)
   - **Reports**: Economic surveys and macroeconomic indicators.

6. **World Bank and IMF Data**
   - **Data Available**: Global economic and labor market data, including India’s unemployment figures and employment trends.
   - **Source**: [World Bank Data](https://data.worldbank.org/) and [IMF](https://www.imf.org/)
   - **Reports**: Economic development reports, labor market analysis.

7. **National Career Service (NCS) Portal**
   - **Data Available**: Job vacancies, demand for different skills, and employment trends in various sectors.
   - **Source**: [NCS](https://www.ncs.gov.in/)

8. **Employment Exchanges in India**
   - **Data Available**: Data on job placements and registration of unemployed individuals in various states.
   - **Source**: State-specific labor exchange portals.

9. **National Sample Survey Office (NSSO)**
   - **Data Available**: Socio-economic data, including workforce, employment conditions, and unemployment metrics.
   - **Source**: [NSSO Surveys](http://mospi.nic.in/national-sample-survey-office-nsso)

10. **Economic Survey of India**
   - **Data Available**: Comprehensive economic data, including unemployment, sectoral employment, and economic growth.
   - **Source**: Ministry of Finance, Government of India
   - **Access**: [Economic Survey Reports](https://www.indiabudget.gov.in/economicsurvey/)


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

