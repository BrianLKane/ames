### PROBLEM STATEMENT
Iowa state law requires that all residential properties in the state be assessed
every two years to determine property tax charges. This high volume of assessment
can be a burden on municipalities. Using predictive modeling as part of the
assessment process could ease this burden.

### EXECUTIVE SUMMARY
We have a strong lasso regression model available for use. Although further
refinement would be beneficial, the model can currently predict within $22,500 of
the target price on average. In its current form, human supervision of the model’s
performance will be particularly necessary for properties over $275,000.

### ADDITIONAL RESOURCES
Documentation of the dataset is available in this directory. Please note that in
the provided Jupyter notebooks, code blocks that perform external write commands
are mostly been commented out to protect against accidental overwrites.

### CONCLUSIONS AND RECOMMENDATIONS
Our analysis began with a relatively clean dataset of over 2,000 home sales in
Ames, IA between 2007 and 2010. We applied a lasso regression model which
highlighted the properties’ above-ground square footage as the most
heavily-weighted feature in predicting sale price. Basement square footage,
the build year, an overall quality rating of “excellent,” and square footage of
finished basement rounded out the most influential features. The model currently
has an r2 score of .914 and an RMSE of 22,421.

Additional exploration of the data and feature engineering will likely improve
the model’s performance, particularly with regards to high-value properties.
As home values near $300,000 the model becomes less reliable. In the absence
of this additional research, the model is currently ready for production on
homes under $275,000.