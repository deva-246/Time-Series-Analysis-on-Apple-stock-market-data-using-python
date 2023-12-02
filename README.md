# Time Series Analysis

Time-series analysis comprises the process and mathematical set of tools used for looking into time-series data to learn not only what happened but also when and why it happened, as well as what is most likely to happen in the future.

## Use Cases for Time-Series Analysis

The “time” element in time-series data means that the data is ordered by time. In this type of data, each entry is preceded and followed by another and has a timestamp that determines the order of the data. Check out our earlier blog post to learn more and see examples of time-series data.

A typical example of time-series data is stock prices or a stock market index. However, even if you’re not into financial and algorithmic trading, you probably interact daily with time-series data.

When you drive your car through a digital toll or your smartphone tells you to walk more or that it will rain, time—series data is part of these interactions.

To illustrate this in more detail, let’s look at the example of health apps.

## Real-World Examples

If you open a health app on your phone, you will see all sorts of categories, from step count to noise level or heart rate. By clicking on “show all data” in any of these categories, you will get an almost endless scroll (depending on when you bought the phone) of step counts, which were timestamped when the data was sampled. ‌‌

This is the raw data of the step count time series. Remember, this is just one of many parameters sampled by your smartphone or smartwatch. While many parameters don’t mean much to most people (yes, I’m looking at you, heart rate variability), when combined with other data, these parameters can give you estimations on overall quantifiers, such as cardio fitness. ‌‌

To achieve this, you need to connect the time-series data into one large dataset with two identifying variables—time and type of measurement. This is called panel data. Separating it by type gives you multiple time series, while picking one particular point in time gives you a snapshot of everything about your health at a specific moment, like what was happening at 7:45 a.m.

## Why Should You Use It?

Now that you’re more familiar with time-series data, you may wonder what to do with it and why you should care. So far, we’ve been mostly just reading off data—how many steps did I take yesterday? Is my heart rate okay? Did it rain yesterday?‌‌

But time-series analysis can help us answer more complex or future-related questions, such as forecasting. When did I stop walking and caught the bus yesterday? Is exercise making my heart stronger? Will it rain tomorrow? ‌‌

To answer these, we need more than just reading the step counter at 7:45 a.m.—we need time-series analysis. Time-series analysis happens when we consider part or the entire time series to see the “bigger picture.” We can do this manually in straightforward cases: for example, by looking at the graph that shows the days when you took more than 10,000 steps this month. ‌‌

But if you wanted to know how often this occurs or on which days, that would be significantly more tedious to do by hand. Very quickly, we bump into problems that are too complex to tackle without using a computer, and once we have opened that door, a seemingly endless stream of opportunities emerges. We can analyze everything, from ourselves to our business, and make them far more efficient and productive than ever.

‌‌
## Time-series components

Let’s go back to our health app example. One thing you may see immediately, just by looking at a time-series analysis chart, is whether your stats are trending upward or downward. That indicates whether your stats are generally improving or not. By ignoring the short-term variations, it's easier to see if the values rise or decline within a given time range. This is the first of the four components of a time series:

Trend: as explained above, a long-term movement of the time series, such as the decreasing average heart rate of workouts as a person gets fitter.
Seasonality: regular periodic occurrences within a time interval smaller than a year (e.g., higher step count in spring and autumn because it’s not too cold or too hot for long walks).
Cyclicity: repeated fluctuations around the trend that are longer in duration than irregularities but shorter than what would constitute a trend. In our walking example, this would be a one-week sightseeing holiday every four to five months.
Irregularity: short-term irregular fluctuations or noise, such as a gap in the sampling of the pedometer or an active team-building day during the workweek.
Time-series analysis visualization with example data in black, trend in red, and the trend with seasonality in blue
Example data in black with the trend in red and the trend with seasonality in blue, cyclic fluctuations, and two large irregularities complete the decomposition (source: author)
Limitations of time-series analysis
If you’re performing time-series analysis, it can be helpful to decompose it into these four elements to explain results and make predictions. Trend and seasonality are deterministic, whereas cyclicity and irregularities are not.

Therefore, you first need to eliminate random events to know what can be understood and predicted. Nothing is perfect, and to be able to capture the full power of time-series analysis without abusing the technique and obtaining incorrect results and conclusions, it’s essential to address and understand its limitations. ‌‌

Generalizations from a single or small sample of subjects must be made very carefully (e.g., finding the time a customer is most likely running requires analyzing the run frequencies of many customers). Predicting future values may be impossible if the data hasn’t been prepared well, and even then, there can always be new irregularities in the future. ‌‌

Forecasting is usually only stable when you consider the near future. Remember how inaccurate the weather forecast can be when you look it up 10 days in advance. Time-series analysis will never allow you to make exact predictions, only probability distributions of specific values. For example, you can never be sure that a health app user will take more than 10,000 steps on Sunday, only that it is highly likely that they will do it or that you’re 95 % certain they will.

## Types of Time-Series Analysis

Time to dive deeper into how time-series analysis can extract information from time-series data. To do this, let’s divide time-series analysis into five distinct types.

**Exploratory analysis**

An exploratory analysis is helpful when you want to describe what you see and explain why you see it in a given time series. It essentially entails decomposing the data into trend, seasonality, cyclicity, and irregularities. ‌‌

Once the series is decomposed, we can explain what each component represents in the real world and even, perhaps, what caused it. This is not as easy as it may seem and often involves spectral decomposition to find any specific frequencies of recurrences and autocorrelation analysis to see if current values depend on past values.

**Curve fitting**

Since time series is a discrete set, you can always tell exactly how many data points it contains.

But what if you want to know the value of your time-series parameter at a point in time that is not covered by your data? ‌‌

To answer this question, we have to supplement our data with a continuous set—a curve. You can do this in several ways, including interpolation and regression. The former is an exact match for parts of the given time series and is mostly useful for estimating missing data points. On the other hand, the latter is a “best-fit” curve, where you have to make an educated guess about the form of the function to be fitted (e.g., linear) and then vary the parameters until your best-fit criteria are satisfied. ‌‌

What constitutes a “best-fit” situation depends on the desired outcome and the particular problem. Using regression analysis, you also obtain the best-fit function parameters that can have real-world meaning, for example, post-run heart rate recovery as an exponential decay fit parameter. In regression, we get a function that describes the best fit to our data even beyond the last record opening the door to extrapolation predictions.

**Forecasting**

Statistical inference is the process of generalization from sample to whole. It can be done over time in time-series data, giving way to future predictions or forecasting: from extrapolating regression models to more advanced techniques using stochastic simulations and machine learning. If you want to know more, check out this article about time-series forecasting.

**Classification and segmentation**

Let’s start with an example: imagine a family sharing one smartwatch for all of the members' runs. The time-series data generated by the watch will have all the family members’ information mixed up. So how would they distinguish each other's runs? Cue in classification and segmentation, although they’re different types of analysis. ‌‌

Classification is looking for patterns in the series and allocating them to a certain number of classes. Segmentation, on the other hand, is separating a time series into a sequence of segments by some desired criteria. ‌‌

In our case, this would be the different runs recorded by the watch. Once the series is split (or segmented) into runs, this becomes a classification problem as each runner will have their unique pattern of speed, stride length, etc., distinguishing them from the rest.‌‌

As you may have already guessed, problems rarely require just one type of analysis. Still, it is crucial to understand the various types to appreciate each aspect of the problem correctly and formulate a good strategy for addressing it.




