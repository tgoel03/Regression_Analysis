# Simple Linear regression
Using real life data set available on Kaggle containing two variables Blood pressure and weight. We need to fit the Simple linear regression between these two variables in R.

#### Importing the data set in R
data<-read.csv(file.choose())

#### View the dataset in R for reference
View(data)

#### To check the head of the data
head(data)

#### To check the data of the particular variable
data$Symbolic.BP

#### Attaching the data
attach(data)

#### To check the correlation between variables
cor(data[,-1])

#### Plotting the graph between variables
plot(Weight,Symbolic.BP,main = "Scatter plot",xlab = "Weight",ylab = "Systolic Pressure")

#### Fitting the Linear model between the variables
slr=lm(Symbolic.BP~Weight)

slr

#### Printing the summary of the model for further analysis
summary(slr)

#### To check the anova table
anova(slr)

#### To get the confidence interval
confint(slr)

#### To draw a straight line
abline(slr)

#### To get the residual
res=residuals(slr)

res

#### To check the assumption of residual
sum(res)

#### To get the fitted values we get from the model
f=fitted.values(slr)

sum(f)

#### For comparison between observed values and fitted values
sum(Symbolic.BP)

#### For visual representation of our model
plot(slr)
