# NYC Parking Violations
### Project Description
### By: Mohammed Almaroof, Siddarth Nalegave, Omar Azeemi, Yossi Watanabe

1.   What is the overarching purpose of your research project, and why is it an important undertaking?
  -   Understand parking violations in New York City and study the various factors and variables that affect the frequency and locality of these parking violations.
  -   We believe that this is an important undertaking because it can help reduce overall parking violations, help prioritize and allocate resources needed to tackle these violations effectively and efficiently.
  -   It can assist with improving policies regarding transportation within the city.
  -   Can help increase city revenue and improve parking enforcement resource allocation.
    

  

2.   How does your research fit into the broader problem domain? You should cite at least 3 papers that help contextualize your research.  
    -   We hope that our research will fit into the broader problem domain of traffic congestion. New York is known for its traffic and is considered as the city with the highest parking violations, and the highest amount of revenue received from parking violations. In 2010 alone, New York made $605 million in parking violations alone. By looking at these trends, we hope that the city can make better decisions according to where more parking accommodation is required, during what times. The following three papers are related to our problem:
	    

		-   Growth or Gridlock: The Economic Case for Traffic Relief & Transit Improvement for a Greater New York
		    

			-   [http://www.pfnyc.org/reports/GrowthGridlock_4pg.pdf](http://www.pfnyc.org/reports/GrowthGridlock_4pg.pdf)
			    
			-   This paper/infographic explains the economics behind how traffic is affecting New York. Talks about the delays that are affecting the community and which areas have the most delays.
		    

		-   Red Zone, Blue Zone: Discovering Parking Ticket Trends in New York City
		    

			-   [https://sites.temple.edu/samackerman/files/2012/10/NYC_parking_Samuel_Ackerman5.pdf](https://sites.temple.edu/samackerman/files/2012/10/NYC_parking_Samuel_Ackerman5.pdf)
			    
			-   This paper talks about trends in parking tickets for the year of 2010. The researcher looks at trends in the geographic distribution of tickets and built a clustergram analysis, to see general trends in who is doing the most violations, which type of car, etc.
		    

		-   Thinking About Congestions
		    

			-   [http://www.streetsblog.org/wp-content/uploads/2015/09/Steer-Davies-Gleave-Congestion-Analysis.pdf](http://www.streetsblog.org/wp-content/uploads/2015/09/Steer-Davies-Gleave-Congestion-Analysis.pdf)
			    
			-   This paper defines congestion, what are the economic and engineering factors of congestion, and how congestion can be measured.
    


3.   What specific hypothesis (hypotheses) are you going to test?
	> 1.Can we accurately predict the frequency of parking violations based on location and time?    
	> 2.Do car color, year, and model affect the likelihood of receiving a parking violation?
    
4.    What are the datasets you'll be working with to answer this question? Please include relevant background describing the datasets you identify.
    
	> The NYC Department of Finance collects data on every parking ticket issued in NYC. The data is made publicly available to aid in ticket resolution and to guide policymakers.	    
	>The dataset includes all the parking violations issued for the fiscal year 2019. This dataset has 43 columns and 6.95 million rows of data. The dataset includes the nature of the violation along with details of the vehicle, location and time.
	> [https://data.cityofnewyork.us/City-Government/Parking-Violations-Issued-Fiscal-Year-2019/pvqr-7yc4](https://data.cityofnewyork.us/City-Government/Parking-Violations-Issued-Fiscal-Year-2019/pvqr-7yc4)
	> We are going to try and understand the correlations that exist within the dataset to figure out what independent variables affect the frequency of parking violations.
    

  

5.   What statistical and machine learning methods do you plan on using to test your hypothesis?
    

	> We are going to use multivariate linear regression models to understand the relation between our dependent and independent variables. We will use forward-selection to select independent variables with high variance and that have the highest impact and effect on the number of parking violations.
	> After selecting the set of independent variables, we will perform the K Nearest Neighbors classifier machine learning method to predict cases of parking violations.
	> Another method we will use is a PolyFit regression model, with multiple polynomials, and see if the data is polynomial in nature.
	> Neural Networks will be used and tested in predicting time series events, such as the time a car might get a ticket, what time streets have most tickets assigned, etc.
  
6.   Who is your target audience for the resource you will build? Depending on the domain of your data, there may be a variety of audiences interested in using the dataset. You should hone in on one of these audiences.
    

	> Our audience is comprised of the general public living in New York City and city officials, including New York’s parking enforcement. Using our resource, people should be able to avoid areas where they are most likely to receive a ticket. 
	> Car buyers will also find benefit, by looking at our resource they will know whether certain models and colors may make them more prone to receiving parking violations. This will allow them to make more informed decisions before purchasing their car. 
	> City officials will gain insight into what areas require new parking, and where exactly their revenue is coming from. For example, city officials could see that one area does not have very many tickets, they would ask the question whether this is because of low levels of enforcement or because of not very much parking? In most instances, a quick Google Maps street view would answer this question. If officials found that there was a lot of parking and not a lot of tickets they could up enforcement in the area, bringing up their revenue.
    

  

7.   What should your audience learn from your resource? Consider specific questions they may want to answer.
	> Parking is particularly difficult in New York City, being that it is one of the busiest cities in the world. For our audience, which is the general public living in New York City, they can learn where to park in the city, according to the time of day, car model, the day of the week, or a number of different features that we will explore in our project. 
	> The most obvious learning point that this project can provide for the intended audience is the probability of receiving a parking violation in a specific area of New York based on a set of features. For a specific subset of the audience, the general public living in the city (particularly commuters), they can use this question to avoid receiving a violation in a part of the city that might be close to their destination. 
	> However, for another subset of the audience, New York’s parking enforcement, they can use this question to reflect on their work, and perhaps target areas that show a low probability of receiving a violation, which might be overlooked by parking enforcement.
    

  
  
  

#### Technical Description

1.   What will be the format of your final web resource (Shiny app, HTML page or slideshow compiled with KnitR, etc.)?
    
	> We will use a Python notebook to perform our exploratory analysis and publish an HTML page using GH pages that contain our report and academic paper.

2.   Do you anticipate any specific data collection/data management challenges?
	> Our dataset is vast, each year’s worth of data contains almost 7 million rows and 42 columns. If we use complex ML algorithms along with polynomial transformation and cross-validation it will take a large amount of time to process.
	> We will need a better method of aggregation to transform the dataset to answer our research question and address our hypothesis.
    

3.   What new technical skills will need to learn in order to complete your project?
	> We want to create heat maps of New York City which highlight areas with the high number of parking violations. We might need to learn new skills to understand and manipulate location and spatial data to achieve this goal, combined with time series forecasting, and learning how to make heat maps in Python.
    

4.   How will you conduct your analysis? Please include a detailed description of your intended modeling approach.
	> The first step of the analysis is finding the distribution of each variable, particularly investigating the correlation index of each variable to the number of violation tickets handed out. Given that this dataset has a relatively large set of features, one of the most essential part of the analysis is feature engineering, ensuring that we are not underfitting or overfitting the data. Feature engineering in this project will mostly rely on domain research, giving us an initial idea of the predictor variables of receiving a parking violation in New York. Coupled with domain research, the project can explore forward and backward selection of features that will determine the best model based on an accuracy score to be chosen going forward. In terms of creating new features, we can use domain research and transformations to create variables we might deem as important.
	> In terms of the machine learning models, the project will use decision trees and k nearest neighbors models to predict receiving parking violations, assessing both models and eventually using the most effective one in terms of accuracy. To split up the data into training and testing sets, the project will use the K fold cross-validation method to ensure the most accurate split of training and testing data. Finally, the project will use grid search to tune the model, and find the best set of parameters (number of neighbors, weights, etc.)
    

5.   What major challenges do you anticipate? 
	> One major challenge we anticipate will be managing such a large dataset. We want to study data from 2014 to 2019 since it can give us a better understanding of trends over time and help improve our prediction and regression models.
	> If we choose to break down the data into a daily aggregate (using count to calculate total violations) we might lose some of the granularity of the data and therefore affect our accuracy. We might also have to look at other data sets with local and spatial information in NYC if we want to incorporate external features that
