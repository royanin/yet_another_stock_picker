## Rite of passage machine-learning project: Yet another stock picker

Stock market is often a gateway to understanding the promises and challenges of machine learning (ML) -- datasets are easy to come by, and you can think of a million ways to slice and dice the data. And then there is the lure of figuring it all out and making money when you are at it! The core of the stock market data is the stock prices, recorded at various intervals, and the volumes of stocks traded. We need to understand how we can handle the time series data to be able to make sense of this problem.


### Dealing with time series data:

From a more technical perspective, this notebook shows a way to analyze time-series data using ML algorithms for a specific class of problems. Time series data are ubiquitous, and usually we want to forecast future values based on the past values. Say, we want to find out the future trend in stock prices (going up or down) of a certain stock, or the high and low temperature next month based on the historical weather data. How do we think about this problem when we have many time series (say, stocks of all Fortune 500 companies, or all US cities with population > 100k), and we want to extract general trends? Extending the weather prediction analogy, we may be interested in finding out if the average temperature next month, when we take the entire planet into account, is going to be a little bit higher than the same month last year, irrespective of their individual variations.

When we are trying to compare many time series, it is useful to construct features out of the time series under investigation, and treat them as any other feature associated with each item.


### Connection with learning analytics:

What brought me to this problem is the need to analyze time-stamped activities of users on an online learning platform. Learner activities have some predictable patterns (e.g., activity spikes before an exam), as well as some less predictable signatures: will an advance learner spend more time on an ungraded activity (becuase the learner takes everything very seriously), or, less time, becuase the learner is busy and has no time to spare? The answer depends on the context, and studying such time-stamped data tells us a lot about the learners and the context. 

Analyzing time series data is a vast field, and the right approach depends on the problem at hand. The rest of the notebook is developed in a way that it's possible to transfer our understanding from the stock market toy problem to learners' timestamped data.

*DISCLAIMER: You won't be able to make any money off the processes shown here in this notebook. But you probably guessed that from the get go!*
