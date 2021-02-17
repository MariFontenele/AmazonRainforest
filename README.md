# AmazonRainforest

**Objective**

The **goal** of this study is to understand **which factors** potentially have impact on **deforestation**. Here, it's going to be examined deforestation **throughout the years 2008 to 2019**. To make sense of the data, **three sources** are going to be considered: 

- **Rural Industry**: the **Agriculture** (acres) and **Cattle** farming (bovine head) data **from 2008 to 2019 per Countie**
- **Social & Economic**: Human Development Index metrics — **HDI**, **Income HDI**, **Education HDI**, **Longevity HDI**; estimated **GDP** per Countie **from 2008 to 2019**
- **Legal protected areas**: spatial data with **indigenous areas** to show if the **deforestation is happening in protected regions**  

**Methodology**

Train **classification** Machine Learning **algorithms** — **Random Forest**, **Extremely Randomized Trees**, **XGBoost** and **CatBoost** — to show which factors are more relevant in predicting **high deforestation** in this period of time  

- The **ground for the analysis** and Machine Learning modelling is the **Counties** of the **Legal Amazon**  
- **Target variable**: the **cumulative deforestation** throughout the years **2008 to 2019**. Since 20% of Counties doesn't have any deforestation focus, the rest of the Counties with deforestation (80%) are going to be divided into quartiles. Therefore, the classification for analysis is: **high-high**, **high-low**, **low-high**, **low-low** and **zero**. However, the **goal is to train the model to predict only the *high-high* class**, so it is going to be **set to True (or 1)** and **all the other classes will be set to False (or 0)**
- **Features**: in harmony with the cumulative deforestation target, the **Agriculture**, **Cattle**, **GDP** and **indigenous areas** proportion during the **years of 2008 to 2019** are also going to be **cumulative** of all the period. Only the **Human Development Indexes** of Counties are going to be **constant**
- **Indigenous areas**: since it is a **spatial data** that shows if the deforestation focus point is occurring in a indigenous reserve, the countie will have a **True** or **False** classification that demonstrates **if any proportion of deforestation** of that countie is happening in **protected reserves**


**Conclusion**

In conformity with the Exploratory Data Analysis, **Cattle farming is overall the most predicting feature for cumulative deforestation in this period of time**

Gross Domestic Product — **GDP** — of the counties is the **second factor** that the algorithms **considered relevant** for predicting high-high deforestation class

In third place, **Education Human Development Index** reveled an interesting **negative correlation** with counties that had the **biggest deforestation** areas during this time 

The fourth place is **Agriculture** that also exhibited a **positive correlation** with counties with greater deforestation; however, this relathionship **is not as significant** as the **Cattle farming**  

It is also worth mentioning that **even though it's not as relevant for prediction**, counties that have **deforestation in indigenous areas**, classification equals to True or 1, demonstrated a **positive correlation with high-high deforestation**

The data is **public available**:

**INPE** - Instituto Nacional de Pesquisas Espaciais: 

- **deforestation**: http://terrabrasilis.dpi.inpe.br/geonetwork/srv/eng/catalog.search#/metadata/a5220c18-f7fa-4e3e-b39b-feeb3ccc4830

- **legal amazon counties map**: http://terrabrasilis.dpi.inpe.br/geonetwork/srv/eng/catalog.search#/metadata/5d16e199-e534-44ca-bcf3-e59964e47b5f

- **indigenous areas**: http://terrabrasilis.dpi.inpe.br/geonetwork/srv/eng/catalog.search#/metadata/5d16e199-e534-44ca-bcf3-e59964e47b5f

**IBGE** - Instituto Brasileiro de Geografia e Estatística

- **official countie's code**: https://www.ibge.gov.br/explica/codigos-dos-municipios.php

- **official countie's area**: https://www.ibge.gov.br/geociencias/organizacao-do-territorio/estrutura-territorial/15761-areas-dos-municipios.html?=&t=downloads

- **official countie's demography**: https://www.ibge.gov.br/estatisticas/sociais/saude/9662-censo-demografico-2010.html?=&t=downloads

- **official legal amazon countie's**: https://www.ibge.gov.br/geociencias/informacoes-ambientais/geologia/15819-amazonia-legal.html?=&t=downloads

- **estimated countie's gdp**: https://sidra.ibge.gov.br/tabela/5938

- **countie's agriculture production**: https://sidra.ibge.gov.br/Tabela/1612

- **countie's cattle farming**: https://sidra.ibge.gov.br/Tabela/73

**ATLAS** - Atlas do Desenvolvimento Humano no Brasil

- **countie's HDI**: http://www.atlasbrasil.org.br/ranking
