## Project Title
Identify Customer Segments (unsupervised ML project)

## by Fan Li

## Date created
Project is created on May 12th 2020.


## Description
In this project, I worked with real-life data provided by our Bertelsmann partners AZ Direct and Arvato Finance Solution. The data here concerns a company that performs mail-order sales in Germany. Their main question of interest is to identify facets of the population that are most likely to be purchasers of their products for a mailout campaign. My job as a data scientist is to use unsupervised learning techniques to organize the general population into clusters, then use those clusters to see which of them comprise the main user base for the company. Prior to applying the machine learning methods, I also assessed and cleaned the data in order to convert the data into a usable form.



## Workflow:

> Step 1: Preprocessing
+ Handling missing data (columns and rows, certain data points that should be treated separately from the rest)
+ Re-Encode Features (feature engineering, one hot encoding)
+ Creating clean pipline

> Step 2: Feature Transformation
+ Impute NaNs
+ Feature scaling (StandardScaler)
+ PCA (cumulative variability assessing result), interpret associations between original features in your dataset based on the weights given on the strongest components.

> Step 3: Clustering
+ KMeans clustering (Elbow method assessing result)
+ Apply the techniques and models that you fit on the demographic data to the customers data: data cleaning, feature scaling, PCA, and k-means clustering. Compare the distribution of people by cluster for the customer data to that of the general population.



## Dataset

* `Udacity_AZDIAS_Subset.csv`:Demographic data for the general population of Germany; 891211 persons (rows) x 85 features (columns).
* `Udacity_CUSTOMERS_Subset.csv`: Demographic data for customers of a mail-order company; 191652 persons (rows) x 85 features (columns).
* `Data_Dictionary.md`: Information file about the features in the provided datasets.
* `ZDIAS_Feature_Summary.csv`: Summary of feature attributes for demographic data.


## Summary of Findings

> Top 3 characteristics that people are more likely to be a customer are:
1. KBA13_ANZAHL_PKW:138.59082167269503
 - (Number of cars in the PLZ8 region)
2. FINANZ_MINIMALIST:3.375807291501999
 - (MINIMALIST: low financial interest--average)
3. SEMIO_VERT:2.4625848727462447
 - (VERT: dreamful--very high affinity)

> Top 3 characteristics that people are less likely to be a customer are:
1. PRAEGENDE_JUGENDJAHRE_decade:-17.843495758711228
- (Dominating movement of person's youth--late 80s)
2. ANZ_HAUSHALTE_AKTIV:-12.277075424326306
- (Number of households in the building--14.0)
3. HH_EINKOMMEN_SCORE:-3.2073500792814666
- (Estimated household net income--low to very low)

We can start to see a clear and reasonable trend here:
> People are more likely to be a customer:
1. live in a region have lots of cars, might be a sign of nice neighborhoods.
2. low financial interest, rated average to low, indicates debt free
3. Very dreamful

**Sum up: young people who is wealthy enough or live with a decent wealthy family**

> people are less likely to be a customer:
1. Was born in late 80s
2. Crowed building with lots of households, might be a sign of low-income neighborhoods
3. Estimated household net income--low to very low

**Sum up: all of above indicate people who are elder and/or have low income.**

 ## About
+ [`Identify_Customer_Segments.ipynb`](https://github.com/victorlifan/Identify_customer_segments-unsupervised-learning-project-/blob/master/Identify_Customer_Segments.ipynb): This is the main file where I performed my work on the project
+ [`Identify_Customer_Segments.html`](https://github.com/victorlifan/Identify_customer_segments-unsupervised-learning-project-/blob/master/Identify_Customer_Segments.html): HTML version of `Identify_Customer_Segments.ipynb`
+ [`support materials`](https://github.com/victorlifan/Identify_customer_segments-unsupervised-learning-project-/tree/master/support%20materials): Data_Dictionary, zipfile data sets

## Software used
+ Jupyter Notebook
+ Atom
+ Python 3.7
> + Sklearn
> + Numpy
> + pandas
> + Matplotlib
> + Seaborn
> + zipfile



## Credits
+ Data provided by: [Arvato Bartlesmann](https://www.bertelsmann.com/divisions/arvato/#st-1) through [Machine Learning - Introduction Nanodegree Program](https://www.udacity.com/course/intro-to-machine-learning-nanodegree--nd229)
+ Instruction and assist: [Machine Learning - Introduction Nanodegree Program](https://www.udacity.com/course/intro-to-machine-learning-nanodegree--nd229)
