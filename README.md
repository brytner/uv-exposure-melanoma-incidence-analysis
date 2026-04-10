# UV Exposure and Melanoma Incidence Analysis

## Overview

<a href="https://www.cdc.gov/radiation-health/features/uv-radiation.html" target="_blank">According to the CDC</a>, UV radiation is classified into three primary types: ultraviolet A (UVA), ultraviolet B (UVB), and ultraviolet C (UVC), based on their wavelengths.<br>
 Almost all the UV radiation that reaches earth is UVA though some UVB radiation reaches earth. UVA and UVB radiation can both affect health, but UVA penetrates deeper into the skin and is more constant throughout the year.

 During my exploration of datasets, I came in contact with <a href="https://www.nature.com/articles/bjc201443" target="_blank">this</a> paper that discusses the effects of cumulative ultraviolet radiation flux in adulthood and risk of incident skin cancers in women based on where they lived.<br> Per author, after careful research and data analysis, they are able to claim that "the risk of incident squamous cell carcinoma (SCC) was positively associated with cumulative UV flux in adulthood. A similar but less pronounced trend was seen for basal cell carcinoma (BCC). **In contrast, incident melanoma risk was not significantly associated with cumulative UV flux."**

The claim in bold above made me curious because according to the <a href="https://www.ncbi.nlm.nih.gov/books/NBK247164/" target="_blank">National Library of Medicine</a> and the <a href="https://www.cdc.gov/skin-cancer/about/index.html" target="_blank">Center for Diseases Control</a>, "melanoma, the third most common type of skin cancer, begins in the melanocytes. Of all types of skin cancer, melanoma causes the most deaths."

This prompted me to propose the question: Is higher long-term UV exposure associated with higher risk for melanoma? Do states in the U.S with the highest measurements of UV light also have the highest incidence rates of melanoma?

This topic interests me because I work in healthcare and I am absolutely fascinated by how risk adjustment, demographic data and actuarial analysis are used to improve patient care, understand trends and even predict future costs for treatment and etc.

This type of real-world scenario peaks my curiosity me and I am very excited to drive into this project.

This project uses health, geographic, demographic, and environmental data to explore the relationship between long-term ultraviolet (UV) exposure and reported melanoma incidence across the United States.

## Datasets

<a href="https://gis.cancer.gov/tools/uv-exposure/uv-county.xlsx" target="_blank">County Level UV Exposure Data for the Continental United States</a><br>
Per dataset description, data includes historical Average Daily Global Solar Radiation estimates (AVGLO) - a proxy measure for UV- in Wh/m² by county in the Continental US for the period 1961-1990 and the more recent 5-year average measures (2019-2024).

<a href="https://www.ers.usda.gov/media/5767/2023-rural-urban-continuum-codes.xlsx?v=79641" target="_blank">Rural-Urban Continuum Codes</a><br>The 2023 Rural-Urban Continuum Codes distinguish U.S. metropolitan (metro) counties by the population size of their metro area, and nonmetropolitan (nonmetro) counties by their degree of urbanization and adjacency to a metro area. The division of counties as either metro or nonmetro, based on the 2023 Office of Management and Budget (OMB) delineation of metro areas, is further subdivided into three metro and six nonmetro categories. Each county and census-designated county-equivalent in the United States, including those in outlying territories, is assigned one of these nine codes. The codes allow researchers, policy makers, and others to view county-level data by finer residential groups—beyond metro and nonmetro—when analyzing trends related to population density and metro influence.

<a href="https://statecancerprofiles.cancer.gov/incidencerates/index.php?stateFIPS=00&areatype=county&cancer=053&race=00&sex=0&age=001&stage=999&type=incd&sortVariableName=rate&sortOrder=default&output=0#results" target="_blank">Melanoma Incidence per County</a><br>
According to the website, "State Cancer Profiles is an interactive map engine produced in collaboration between the National Cancer Institute and Centers for Disease Control and Prevention. It was developed with the goal to provide a geographic profile of cancer burden in the United States and reveal geographic patterns of cancer incidence, mortality, risk factors for cancer, and cancer screening, across different population subgroups."


<a href="https://seer.cancer.gov/data-software/documentation/seerstat/nov2024/" target="_blank">SEER\*Stat Databases: SEER November 2024 Submission</a><br>
This dataset was obtained through the SEER*StatApplication, a software from the **Surveillance, Epidemiology, and End Results Program (SEER)**, a premier source of population-based cancer statistics in the United States. It contains detailed and well documented cancer records with adjustable variables.

## Analysis Constraints and Considerations

While this analysis uses reputable sources, such as SEER and data from official government agencies, there are limitations to consider when interpreting the results:<br>

### Patient Mobility

This analysis assumes that a patient's county of diagnosis is also a reflection of their long term living arrangements.<br>
Therefore, this analysis does not consider that patients may have relocated across counties or states prior to diagnosis or that long-term exposure might not align with the recorded location.

### Data Restrictions due to Geographical Reasons

Due to privacy protections of Patient Health Information, SEER restricts the access of certain level of data due to geographical reasons.<br>
For example, certain public datasets have regions that are suppressed, unavailable or restricted at county level.<br>
This ensures that patients living in not densely populated counties have their privacy protected but also leads to incomplete geographic coverage or reduced precision in spatial analysis.

### Additional Considerations

The findings in this project should be viewed as descriptive, exploratory, useful for identifying patterns and hypotheses.<br>

This project is just the foundation for future work that will potentially incorporate more granular data where permitted, integration of machine learning models to enhance predictive capabilities such as future UV exposure forecasting using historical trends or training models on historical SEER and environmental data to identify patterns associated with melanoma incidence.<br>
This will shift the project from descriptive analysis to a more predictive and analytical framework that follows the trends in the real-world of data analytics.

## How to access the project

1 - Clone this repository.<br>
<br>
2 - Install the required Python packages:<br>
        `pip install -r requirements.txt`<br>
        <br>
3 - Open *uv-exposure-melanoma-incidence-analysis.ipynb* in Jupyter Notebook or JupyterLab.
