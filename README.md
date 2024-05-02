# Relatedness and Product Complexity Meet Gravity Models of International Trade

Authors: Marek Tiits, Tarmo Kalvet, Chahinez Ounoughi, and Sadok Ben Yahia

Journal of Open Innovation: Technology, Market, and Complexity (ELS)

---

## Bilateral Trade Dataset Description

In this experiment, we utilized a comprehensive dataset obtained from UN Comtrade and supplemented it with relevant variables from the CEPII gravity dataset. Below, we provide an overview of the dataset and the preprocessing steps applied to ensure its quality and relevance:

- **Data Cleaning Process:** During the data cleaning process, we applied specific criteria to ensure the accuracy and relevance of our dataset. These criteria included:
  - Downloading the UN Comtrade monthly data using the H4 revision.
  - Selecting data for the period from 2016 to 2021.
  - Focusing on general trade patterns by choosing data with:
    - Customs Procedure Codes (CustomsCode) set to C00.
    - Modes of Transport (MotCode) set to 0.
    - Last Known Destinations (Partner2Code) set to 0, if multiple destinations were present.

- **Incorporated Variables:** In addition to the cleaned and simplified features, we incorporated relevant variables from the CEPII gravity dataset. These variables included:
  - Harmonic distance (measuring distance between trading partners).
  - 'Contig' (indicating if countries share a border).
  - 'gdp_o' and 'gdp_d' (Gross Domestic Product of exporting and importing countries).
  - 'gdpcap_o' and 'gdpcap_d' (GDP per capita of exporting and importing countries).
  - 'pop_o' and 'pop_d' (Population of exporting and importing countries).
  - 'wto_o' and 'wto_d' (Membership in the World Trade Organization).

- **Data Standardization:** To ensure better comparability and interpretation of the data, we standardized values by dividing all dollar values by 1,000,000, specifically for features such as GDPs and trade values.

- **Product Complexity and Relatedness Density:** We also incorporated measures of product complexity ('pci') and relatedness density ('density') into our analysis. These features provide insights into the sophistication of traded goods and the proximity of products to a country's export portfolio, respectively.

- **Summary of Dataset:**

  - **Period:** 2016-2021
  - **Reporter Code:** 148
  - **Partner Code:** 203
  - **Commodity Code:** 5,203
  - **Size:** 
    - Exports: 256,300,077 records
    
  - **Variables:**
    - Trade Value
    - Year
    - Month
    - Commodity Code
    - GDP
    - GDP per capita
    - Population
    - Harmonic distance
    - Contiguity
    - WTO membership
    - PCI (Product Complexity Index)
    - Density (Relatedness Density)


This comprehensive dataset forms the basis of our analysis and allows us to explore various aspects of international trade patterns.



# Repository Structure

This repository is organized into one main folder: "Exports" containing notebooks and analyses related to the project. Below, you'll find a breakdown of the folder structure and the purpose of each notebook:


## Exports Folder

1. - **Data Analysis [Correlation & Distribution].ipynb:** This notebook provides a comprehensive data analysis, including correlation and distribution analyses, for the export data.

2. **DT and Features Selection Notebook:**
   - *DT and Features Selection.ipynb:* This notebook is dedicated to the Decision Tree (DT) model and an in-depth analysis of features.

3. **RF Experiments with Standard 20% Split Notebook:**
   - *RF Experiments with Standard 20% Split.ipynb:* This notebook documents the Random Forest (RF) experiments conducted using the standard 20% data split for training and testing.

4. **RF Experiments with Completely Unseen 2021 Test Set Notebook:**
   - *RF Experiments with Completely Unseen 2021 Test Set.ipynb:* Here, you'll find the RF experiments performed using a test set from 2019 that was completely unseen during the model's training phase.


This organized structure allows for easy access to the specific experiments and analyses carried out for your project. You can explore and refer to these notebooks as needed for a comprehensive understanding of your research.

## Requirements and Software

To reproduce the experiments and analyses conducted in the notebooks within this repository, you'll need to ensure that you have the following software and libraries installed in your Python environment:

- **Python 3.10:** Python is the programming language used for data manipulation, analysis, and modeling.

- **Pandas 2.0.3:** Pandas is a powerful library for data manipulation and analysis. We use it extensively for data preprocessing, handling datasets, and organizing data structures.

- **NumPy 1.25.0:** NumPy is a fundamental library for numerical operations in Python. It plays a crucial role in handling arrays and performing mathematical operations efficiently.

- **Scikit-Learn (sklearn) 1.2.2:** Scikit-Learn is a versatile machine learning library. We rely on it for implementing various machine learning algorithms, including Decision Trees and Random Forests.

- **Matplotlib 3.7.1:** Matplotlib is a popular library for creating static, animated, or interactive visualizations in Python. We use it to visualize data, including plots and graphs.

- **Seaborn 0.12.2:** Seaborn is a data visualization library based on Matplotlib. It provides a high-level interface for creating attractive and informative statistical graphics.

### Purpose:

- **Python 3.10:** The primary programming language used for scripting, data analysis, and running experiments.

- **Pandas 2.0.3:** Pandas is essential for data cleaning, manipulation, and organization, ensuring that data is in the right format for analysis.

- **NumPy 1.25.0:** NumPy handles numerical computations efficiently and is crucial for working with arrays and matrices.

- **Scikit-Learn (sklearn) 1.2.2:** Scikit-Learn provides a wide range of machine learning algorithms, which we use for modeling and evaluating our Decision Tree and Random Forest models.

- **Matplotlib 3.7.1:** Matplotlib is utilized to create various data visualizations, aiding in the interpretation and presentation of results.

- **Seaborn 0.12.2:** Seaborn enhances data visualization with more aesthetically pleasing and informative statistical plots, improving the clarity of our analyses.

Make sure to install these libraries and maintain the specified versions to replicate the experiments and analyses accurately.



## Acknowledgments
This work was supported by grants to TalTech – TalTech Industrial (H2020, grant No 952410) [https://taltech.ee/arikorralduse-instituut/taltech-industrial] and Estonian Research Council (PRG1573)[https://www.etis.ee/Portal/Projects/Display/2f7d9acc-95c7-4285-af62-6e7b86ab0919
].

## Citation
```bibtex
@article{TIITS2024100288,
  title = {Relatedness and Product Complexity Meet Gravity Models of International Trade},
  journal = {Journal of Open Innovation: Technology, Market, and Complexity},
  pages = {100288},
  year = {2024},
  issn = {2199-8531},
  doi = {https://doi.org/10.1016/j.joitmc.2024.100288},
  url = {https://www.sciencedirect.com/science/article/pii/S2199853124000829},
  author = {Marek Tiits and Tarmo Kalvet and Chahinez Ounoughi and Sadok Ben Yahia},
  keywords = {Economic development policy, Relatedness and Complexity, Gravity model, Machine-learning, Explainability},
  abstract = {Researchers have long used gravity models to analyze international trade patterns, identify export opportunities, and negotiate trade agreements. Recent research has emphasized the significance of relatedness and product complexity research in developing robust economic development strategies. This paper presents a novel approach, incorporating relatedness and product complexity as integral elements for interpreting export potential within gravity models powered by machine learning. Our approach stands out for its proficiency in accurately predicting bilateral trade values at a detailed product group level, providing valuable insights for policymakers and other stakeholders. The research leverages random forest machine learning models for predictions and incorporates relatedness and complexity to reveal new dimensions in international trade analysis.}
}

