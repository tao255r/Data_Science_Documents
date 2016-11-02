## <font color="MediumSlateBlue"> General Data Exploration Process </font>    

### <font color="lighblue"> Variables Identification </font>   
* Identify independence variables and data types
* Identify dependence variabl and data type
* Data types: norminal, ordinal, interval/ratio

### <font color="lighblue"> Univariate Analysis (look at variables by itself) </font>
* Continuous Variable
	* Central Tendency: Mean, Median, Mode, Min, Max  
	* Measure of Dispersion: Range, Quartile, IQR, Variance, Standard Deviation, Skewness and Kurtosis  
	* Visualization: Histogram, Box Plot  

* Categorical Variable  
	* Count and Count % against each category
	* Bar chart can be used as visualiaztion 

* Missing Value
	* Identify reasons for missing value
		* Data Extraction
		* Data Collection
			* Missing completely at random: This is a case when the probability of missing variable is same for all observations. For example: respondents of data collection process decide that they will declare their earning after tossing a fair coin. If an head occurs, respondent declares his / her earnings & vice versa. Here each observation has equal chance of missing value.
			* Missing at random: This is a case when variable is missing at random and missing ratio varies for different values / level of other input variables. For example: We are collecting data for age and female has higher missing value compare to male.
			* Missing that depends on unobserved predictors: This is a case when the missing values are not random and are related to the unobserved input variable. For example: In a medical study, if a particular diagnostic causes discomfort, then there is higher chance of drop out from the study. This missing value is not at random unless we have included “discomfort” as an input variable for all patients.
			* Missing that depends on the missing value itself: This is a case when the probability of missing value is directly correlated with missing value itself. For example: People with higher or lower income are likely to provide non-response to their earning.
	* Treatment for missing values
		* Deletion (delete the whole observation)
			* Deletion methods are used when the nature of missing data is “Missing completely at random” else non-random missing values can bias the model output.
		* Mean/ Mode/ Median Imputation
		* Use Prediction Model
			* The model estimated values are usually more well-behaved than the true values
			* If there are no relationships with attributes in the data set and the attribute with missing values, then the model will not be precise for estimating missing values.
		* KNN Imputation
			* Advantages: 
				* k-nearest neighbour can predict both qualitative & quantitative attributes
				* Creation of predictive model for each attribute with missing data is not required
				* Attributes with multiple missing values can be easily treated
				* Correlation structure of the data is taken into consideration
			* Disadvantage:
				* KNN algorithm is very time-consuming in analyzing large database. It searches through all the dataset looking for the most similar instances.
				* Choice of k-value is very critical. Higher value of k would include attributes which are significantly different from what we need whereas lower value of k implies missing out of significant attributes.

* Outlier Detection
	* Outlier can be of two types: Univariate and Multivariate.
		* Univariate outliers can be found when we look at distribution of a single variable. 
		* Multi-variate outliers are outliers in an n-dimensional space. In order to find them, you have to look at distributions in multi-dimensions.
	* Detect Outliers
		* Visualization : Box-plot, Histogram, Scatter Plot
		* Analysts
			* Any value, which is beyond the range of -1.5 x IQR to 1.5 x IQR
			* Use capping methods. Any value which out of range of 5th and 95th percentile can be considered as outlier
			* Data points, three or more standard deviation away from mean are considered outlier
			* Bivariate and multivariate outliers are typically measured using either an index of influence or leverage, or distance. Popular indices such as Mahalanobis’ distance and Cook’s D are frequently used to detect outliers.
	* Remove Outliers
		* Deleting observations
		* Transforming and binning values (like: log)
		* Imputing (remove outlier then impute)
		* Treat separately: If there are significant number of outliers, we should treat them separately in the statistical model.

### <font color="lighblue"> Bivariate Analysis (look at 2 variables at the same time, normally each IV vs. DV) </font>
* Continuous & Continuous
	* Scatter plot
	* Correlation: strength of relationship
* Categorical & Categorical
	* Two-way table (with count%)
	* Stacked Column Chart
	* Chi-Square Test
* Categorical & Continuous
	* Z-Test/ T-Test (whether mean of two groups are statistically different from each other or not). 
		* T-test is very similar to Z-test but it is used when number of observation for both categories is less than 30.
	* ANOVA (whether the average of more than two groups is statistically different).

### <font color="lighblue"> Feature Engineering </font>
* Variable transformation
	* Change the scale of a variable or standardize the values of a variable for better understanding.
	* Transform complex non-linear relationships into linear relationships. (like: Log transformation)
	* Symmetric distribution is preferred over skewed distribution.
		* For right skewed distribution, we take square / cube root or logarithm of variable
		* For left skewed, we take square / cube or exponential of variables.
	* Binning of Variables: dividing dataset into groups and model separately.
	* Common transformation methods: Logarithm, Square / Cube root, Binning
* Variable / Feature creation or reduction
	* Create variables for difference in date, time and addresses
	* Create new ratios and proportions: Input / Output (past performance), productivity, efficiency and percentages
	* Check variables for seasonality and create the model for right period

## <font color="MediumSlateBlue"> Data Partition </font> 
* Separate data into training, validation and testing. Could be only training and testing depends on project. 

## <font color="MediumSlateBlue"> Training Model </font>
* Important analysis:  Boruta
* Classification models
* Regression models
* Ensemble methods
* Unsupervised learning models
* Hyperparameter Optimization

## <font color="MediumSlateBlue"> Evaluation and Adjustment </font>
* Cross-validation
* Regression Evaluation Matrix
* Classification Evaluation Matrix    

<font color="DarkGray"> (... to be continue...) </font> 