# Unsupervised_challenge

Determine which cryptocurrencies are on the trading market and determine whether they can be grouped to create a classification system for an investment model

## Data Preperation

The CSV file was loaded and steps were taken to clean the data; Filtering was completed to reveal 532 currencies that are tradable. To arrive at this number, rows containing null values were removed along with coins that have not been mined(i.e. coins mined > 0). The 'CoinName' column was purged from the data set due to the nature of coin names themselves not contributing to the analysis of the data. To accomodate the numeric applications of the machine learning algorithm columns with text values were converted to numeric using Pandas to create dummy variables

## Dimensionality Reduction

In response to the increase in the number of features, as a consequence from creating dummy variables in the data set, dimensionality reduction techniques were utilized to reduce the number of features mathematically in an attempt to mute the 'noise' in our model before clustering. Principle Component Analysis was utilized to preserve 90% of the explained variance by reducing the data set to 73 features.

TO further reduce the number of features T-SNE was used and the results are ambiguous. Some clustering can be defined but it is not clear. 

## Cluster analysis with k-means and conclusion

An elbow plot was generated in an attempt to identify a numbner of clusters. From the generated plot it appears the elbow reduces in inertia at a k value of 3. The results were then visualized for analysis.

There is evidence of faint clustering in cryptocurrencies, however it is not a strong enough clustering to implement and invest in a classification trading model for cryptocurrencies
