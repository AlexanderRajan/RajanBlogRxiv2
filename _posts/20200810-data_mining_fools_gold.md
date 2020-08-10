---
published: false
permalink: /_posts/fools_gold
---
# [Data mining fool’s gold - Gary Smith](https://journals.sagepub.com/doi/abs/10.1177/0268396220915600)

Data mining fool's gold, by [Gary Smith](https://garysmithn.com/) highlights several issues with data mining, and the failures of data scientists (and other researchers) to be aware of and mitigate these dangers.

Smith's invited [article](https://journals.sagepub.com/doi/abs/10.1177/0268396220915600) in the [Journal of Information Technology](https://journals.sagepub.com/home/jina) highlights several patterns that are endemic to data science: failure of ML methods to distinguish between correlation vs causation, post-hoc rationalization by researchers, and the statistical likelihood of feature selection methods to identify meaningless relationships as the scale of data increases. He posits that the reversal of the scientific method (putting data before theory) leads to a lot of false positives in identifying meaningful relationships from clusters and correlations, which in turn are wasteful (in time and resources).

These risks are extended to NLP (natural language processing; eg, predicting the stock market from Trump's tweets) and image recognition (eg, facial recognition), and how they contribute to the broader reproducibility crisis in science.

Smith's article clearly lays out several problems and walks the reader through some simulations to highlight how spurious correlations are detected. In particular, he walks through an example sequential data mining steps continue to find improbable and illogical relationships between Trump's tweets and the stock market

While data mining may be a logical first step, it cannot be the only step before brining a product to market, even when validated with out-of-sample data. As Smith shows, the more nuisance variables that exist in a dataset, the more features will be found to predict an outcome. The problems here are three-fold: nuisance variables will be selected as informative, true variables will be crowded out, and inevitably some nuisance variables will survive both in-sample and out-of-sample testing. Thus, iterative or sequential data mining and validatation will both include spurious correlations, and crowd out actual (useful) predictors.

Often, when predictive performance does eventually (and often inevitably) begin to fail, instead of acknowledging the failures of data mining, groups instead double-down, rerunning their feature selection and model fitting algorithms, and touting them as "flexible and innovative."
> The Journal attributed Voleon’s struggles to the fact that financial markets are “continually being affected by new events, the relationships among which are frequently shifting.” This is a common excuse when data-mined patterns vanish—the world has changed. Perhaps, but an alternative explanation is that the statistical patterns that data-mining algorithms discover were fleeting because they were fortuitous.
Another justification is "we've now sampled more broadly, and therefore have found better predictors."

These problems are pervasive in biotech and health care as well. For example:
> Google researchers created a data-mining program called Google Flu Trends that analyzed 50 million search queries and identified 45 key words that “can accurately estimate the current level of weekly influenza activity in each region of the United States, with a reporting lag of about one day” (Ginsberg et al., 2009)
> However, after issuing its report, Google Flu Trends over-estimated the number of flu cases for 100 of the next 108 weeks, by an average of nearly 100% (Lazer et al., 2014). Google Flu Trends no longer makes flu predictions.

In another example, "The algorithm changes constantly because it has no logical basis and is continuously buffeted by short-lived correlations."

Another problem that Smith briefly hits on, which is growing within biomedical science, is [HARKing](https://en.wikipedia.org/wiki/HARKing)(Hypothesizing After the Results are Known), in which researchers concoct post-hoc rationalizations for data mined results. This is closely related to many evolutionary or psychological explanataions: coming up with "just-so" stories to explain or concoct a mechanism by which results are logical, or even in the absence of data, as described by [Steven J Gould](https://www.newyorker.com/magazine/2012/09/17/it-aint-necessarily-so).

Here's one of my favorite articles describing HARKing, here in the [context of genomics](https://onlinelibrary.wiley.com/doi/full/10.1002/gepi.22189), a favorite largely because of the inflammatory title ["Spinning convincing stories for both true and false association signals"](https://onlinelibrary.wiley.com/doi/full/10.1002/gepi.22189) and because it is open access!
> “All that glitters is not gold”—one might interpret apparent patterns in the data as plausible even when the peak is a false positive.

I should add, in closing, that this is not a general indictment of data science, machine learning, data mining, or exploratory analyses. Rather, it is a warning against leaping to conclusions from what should be considered an initial analysis, and certainly against productionalizing or bringing to market something based solely on data mining.