# Project Proposal \- Nuclear Energy Project

### Purpose

This project analyzes whether nuclear energy is necessary to meet rising global electricity demand in the coming decades, while remaining in line with international emissions goals. The analysis examines both the global picture and regional disparities, recognizing that the answer may differ significantly between advanced economies and fast-growing developing regions such as South and Southeast Asia and Sub-Saharan Africa.

### Approach & Methodology

The project follows a five-phase structure. First, data from three sources is collected and cleaned into a unified pipeline. Second, an exploratory data analysis establishes the current global energy mix by technology and region. Third, three parallel analysis modules are built: an energy mix analysis, a demand gap model comparing IEA scenario projections against a bottom-up renewable buildout projection derived from GEM pipeline data, and a nuclear pipeline analysis assessing how much planned capacity will realistically come online based on historical delivery rates. Fourth, GIS visualizations map the spatial distribution of current and pipeline energy infrastructure and highlight regions where the projected supply falls short of demand. Fifth, the findings are synthesized into a data-driven verdict on nuclear necessity. 

### Data Sources

*This project draws on three open datasets:*

* **Global Energy Monitor (GEM)** — the Global Integrated Power Tracker (GIPT) and Global Nuclear Power Tracker (GNPT), providing unit-level data on power plants worldwide including capacity, status, fuel type, location, and development timeline.   
* **IEA World Energy Outlook 2025 (WEO)** — two CSV files covering global and regional electricity demand projections across three scenarios (Current Policies, Stated Policies, and Net Zero Emissions by 2050\) up to 2050\.  
* **Energy Institute Statistical Review of World Energy 2025** — historical energy production and consumption data by country and fuel type from 1965 to 2024, used as a cross-check on current trends and for demand trend modeling.

### Tech stack

The project is built entirely in Python, using Jupyter notebooks as the primary working environment. Key libraries include pandas and GeoPandas for data wrangling and spatial processing, Folium and Plotly for interactive maps and visualizations, Matplotlib and Seaborn for EDA charts, and Scikit-learn for trend modeling. Data is stored in Parquet format for efficiency. 

### Literature (so far)

- [iea.org/reports/nuclear-power-and-secure-energy-transitions](http://iea.org/reports/nuclear-power-and-secure-energy-transitions)   
- [https://aben.com.br/wp-content/uploads/2022/02/Nuclear-energy-a-pathway-towards-mitigation-of-global-warming.pdf](https://aben.com.br/wp-content/uploads/2022/02/Nuclear-energy-a-pathway-towards-mitigation-of-global-warming.pdf)  
- [https://www.iaea.org/newscenter/news/five-reasons-the-clean-energy-transition-needs-nuclear-power](https://www.iaea.org/newscenter/news/five-reasons-the-clean-energy-transition-needs-nuclear-power)  
- [https://www.mdpi.com/1996-1073/15/12/4275](https://www.mdpi.com/1996-1073/15/12/4275)  
- [https://www.cell.com/heliyon/fulltext/S2405-8440(22)00376-0](https://www.cell.com/heliyon/fulltext/S2405-8440\(22\)00376-0) 