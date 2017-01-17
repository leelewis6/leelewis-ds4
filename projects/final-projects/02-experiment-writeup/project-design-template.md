# Project Design Writeup and Approval Template

Follow this as a guide to completing the project design writeup. The questions for each section are merely there to suggest what the baseline should cover; be sure to use detail as it will make the project much easier to approach as the class moves on.

### Project Problem and Hypothesis
* What's the project about? What problem are you solving?
    * This project is in the field of real estate. Given several features,the goal is to predict the sales price of homes sold in Ames, Iowa from 2006 to 2010 

* Where does this seem to reside as a machine learning problem? Are you predicting some continuous number, or predicting a binary value?
    This is a regression problem. I'm predicting a continuous number - Sales Price. 

* What kind of impact do you think it could have?
    Identifying a resonable sales price for a residential property is very important for real estate agents or those selling the property. It is especially impactful for those that build predictive models to determine if they should rennovate/flip a home. These types of models would help investors minimize the risk of losing money on flips. 

* What do you think will have the most impact in predicting the value you are interested in solving for?
    I suspect square footage, the size of the lot, and number of bedrooms/bathroom will have the strongest predictive power. 

### Datasets
* Description of data set available, at the field level (see table)
    Please see the Real_Estate_Data_Dict.csv, in the same path as this file. 

* If from an API, include a sample return (this is usually included in API documentation!) (if doing this in markdown, use the javacription code tag)

### Domain knowledge
* What experience do you already have around this area?
    My wife and I recently rennovated a home and we are in the process of selling it. Other than comps, we've had a difficult time detrmining a reasonable sales price. 

* Does it relate or help inform the project in any way?
    It is defintely related. I'm also interested in predicting who will purchase the home, as a potential extensnsion to this project. This project was focus solely on predicting sales price. 

* What other research efforts exist?
    * Use a quick Google search to see what approaches others have made, or talk with your colleagues if it is work related about previous attempts at similar problems.
    * This could even just be something like "the marketing team put together a forecast in excel that doesn't do well."
    * Include a benchmark, how other models have performed, even if you are unsure what the metric means.
    
    Generally speaking, other predictive models in this space use less features and are very specific to the geographic location or continue less features than our Iowa data set.  A few examples:

1. http://ww2.amstat.org/publications/jse/v16n2/datasets.pardoe.pdf
2. http://lib.stat.cmu.edu/DASL/Datafiles/homedat.html
3. http://fic.wharton.upenn.edu/fic/papers/10/10-01.pdf


### Project Concerns
* What questions do you have about your project? What are you not sure you quite yet understand? (The more honest you are about this, the easier your instructors can help).
    I have an extensive data dictionary that explains all of the variables. Those I've never heard of, are very intuitive. 

* What are the assumptions and caveats to the problem?
    * What data do you not have access to but wish you had?
    I would like to consider adding some type of data that indicates the power of the financial market. Perhaps an index form the NYSE, or other reputable source. I may also consider including interest rates as well. I would assume, prices are going to be higher when interest rates are low. 

* What is already implied about the observations in your data set? For example, if your primary data set is twitter data, it may not be representative of the whole sample (say, predicting who would win an election)

    This data set is collected for a specific city in Iowa. The breadth of data may not be available for other cities, which makes this model flawed and makes it very difficult to make predictions for other cities. During investigation, we may find that there are only a few significant variables, that are avaiable for properties in most major cities. 

* What are the risks to the project?
    * What's the cost of your model being wrong? (What's the benefit of your model being right?)
    * Is any of the data incorrect? Could it be incorrect?
    There are sources that indicate that data from the Assessor's office ( which is the source of this data set) can have minior discprenscies. Generally speaking, the data is considered acccurate. 

### Outcomes
* What do you expect the output to look like?
    As metioned earlier in this analysis, I woudl expect the square footage of the home, the size of the lot, and the number of bedrooms/bathrooms will have a positive correlation on price. I would also expect interest rates to have a negative corrleation with sales price - low rates, higher prices. 


* What does your target audience expect the output to look like?
    I suspect my target audience will have similar assumptions about the anticipated output. 

* What gain do you expect from your most important feature on its own?
    Square footage, based on experience, is the best indicator of sales price, as many prices are based on cost per square foot. 

* How complicated does your model have to be?
    I suspect there will be a fair amount of feature engineering required to achieve a model with the lowest MSE. I'd like to reduce the number of varaibles by analyzie correlation and/or applying PCA.  Out of the 82 variables, I would suspect 20 to 30 will be very significant. 

* How successful does your project have to be in order to be considered a "success"?
    The model has to include features that are readily available for homes in most major cities. If I include features that are rarely documented, my model won't be flexible and will not be leveraged outside of Ames, Iowa. 

* What will you do if the project is a bust (this happens! but it shouldn't here)?
    I'll simplify the model to avoid collinearlity and ensure the features included have a strong corrleation to sales price. 


