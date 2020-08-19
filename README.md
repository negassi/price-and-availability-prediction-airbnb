## To accomplish this challenge, the process is divided into three major tasks:

> Data Wrangling. <br>
> Exploratory Data Analysis.<br>
> Predictive Modeling

And each task is done into separate files and this files is for Data Wrangling.

Data wringling: <br> Data wrangling is a process of making raw data ready for data analysis.In this process the following tasks will be done

Column wise operation
> Remove unimportant columns. <br>
> All columns with that has the text 'url' will be removed. <br>
> All columns that have constant values will be removed. <br>
> All columns with missing values more than 40% will be removed <br>
> Dollar sign and percent sign will be remved from numerical data <br>
> Text/commnet variables will be removed for this step(some of them will be added later with NLP process/ sentimental analysis <br>
> Other variables will be individually inspected and will be hand picked to the model. <br>
> Only 'availability_30' will be selected and the other 'availability' columns will be removed. <br>
Row wise operation
> If columns have more than 20% and less than 40% of missing, their respective rows will be removed. <br>
> If columns have less than 20% missing values, their respective rows will be imputed. Numerical columns will pick the mean of the available values and categorical will pick a value that is most frequent. <br>
> The columnd 'security_deposit' with missing values will be considered as no security deposit is needed to book. as a result zero will be imputed to missing security deposit.
Calcuated fields <br>
> The dates 'host_since' and 'calendar_last_scraped' will be used to calculate the 'host_experience' and will be removed. <br>
> The dates 'first_review' and 'last_review' will be used to calculate 'review_duration' and will ber removed. <br>
Transformation
> The column 'amenities' will be vectorized to columns 'parking','lounge', 'breakfast', 'beachfront', 'dryer', 'fittness'. <br>
Data consistency
> The 'availability_30' column values should have values of range between 0 and 30 days. And also it also should be checked agains 'host_experience' column. host experience should be greater than availability.

Exploratory Data Analysis
For data explotation purpose, I will use the following graphs.

> 'jointplot': To show how price and availabilit are distributed against each other.<br>
> 'boxplot': To see how price and availability change with property type and room type.<br>
> 'distplot': To see how price and availability are distributed for different cancellation policies.<br>


Predictive Modeling

> I will use 5 learner models with differnt parameters to achieve maximum peroformance. Price is continuous variable as a result I will use a regression technique and will use RMSE as comparison metrics.
> Availablity will be transformed to categorical variable 0 for non availability and 1 other wise.I will use classification technique will choose accuracy as comparison technique.


Finally
> To achieve maximum performance of prediction, a good domaing knowledge is very important. I tried to investigate the nature of data both from internet and my intuition. I strongly believe if more time was given on the variable selection, handling the missing values, and some calculated field operation would give an improved result. And also, some spatial analysis could be done. For example given the date and location of the data, we could see price and availability change for different places during summer and winter.
