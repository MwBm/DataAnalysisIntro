# DataAnalysisIntro

Motivated by personal experiences at Disneyland, I conducted an analysis of the relationship between temperature and ride wait times using a publicly available Kaggle dataset. After cleaning the dataset with Pandas, I performed an initial exploratory analysis using Matplotlib to identify patterns and trends.

To quantify the relationship between temperature and wait times, I conducted a Pearson correlation test, which revealed a weak linear relationship (correlation coefficient: 0.16). Recognizing the potential influence of the dataset's size and variability, I segmented the data into four temperature ranges and analyzed the new groupings using pivot tables and visualizations.

Given the observed non-normality in the data, I employed a Kruskal-Wallis H test, which demonstrated statistically significant differences in wait times across temperature categories (H-statistic: 187, p < 0.01). These findings indicate that temperature can meaningfully influence wait times, offering valuable insights for optimizing ride schedules to minimize wait times.

Leveraging this analysis, I developed a predictive model to estimate wait times based on weather and other influencing factors. The process began with analyzing a correlation matrix and importances to determine which columns I needed to keep. Overall, I decided to keep a large majority based on the importances. The dataset was then standardized to mitigate any disproportionate influence from variances in column magnitudes. Using a RandomForestRegression algorithm, I trained the model on the cleaned data. The initial model achieved an R-Squared value of .58, indicating a reasonable starting point with opportunities for refinement. Future iterations will prioritize improving model accuracy.
