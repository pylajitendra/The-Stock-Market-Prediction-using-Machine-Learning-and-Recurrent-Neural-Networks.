# The-Stock-Market-Prediction-using-Machine-Learning-and-Recurrent-Neural-Networks.

**Data:**

**The Google Stock Price Test and Train Data:**

Date,Open,High,Low,Close,Volume
1/3/2017,778.81,789.63,775.8,786.14,"1,657,300"
1/4/2017,788.36,791.34,783.16,786.9,"1,073,000"
1/5/2017,786.08,794.48,785.02,794.02,"1,335,200"
1/6/2017,795.26,807.9,792.2,806.15,"1,640,200"
1/9/2017,806.4,809.97,802.83,806.65,"1,272,400"
1/10/2017,807.86,809.13,803.51,804.79,"1,176,800"
1/11/2017,805,808.15,801.37,807.91,"1,065,900"
1/12/2017,807.14,807.39,799.17,806.36,"1,353,100"
1/13/2017,807.48,811.22,806.69,807.88,"1,099,200"
1/17/2017,807.08,807.14,800.37,804.61,"1,362,100"
1/18/2017,805.81,806.21,800.99,806.07,"1,294,400"
1/19/2017,805.12,809.48,801.8,802.17,"919,300"
1/20/2017,806.91,806.91,801.69,805.02,"1,670,000"
1/23/2017,807.25,820.87,803.74,819.31,"1,963,600"
1/24/2017,822.3,825.9,817.82,823.87,"1,474,000"


**The Machine Learning Stock Prediction System with Recurrent Neural Networks:**

**Introduction:**


This article explores a Machine Learning algorithm called Recurrent Neural Network (RNN), it's a common Deep Learning technique used for continuous data pattern recognition. Recurrent Neural Network take into account how data changes over time, it's typically used for time-series data (stock prices, sensor readings, etc). Recurrent Neural Network can also be used for video analysis.


I provided with a dataset consisting of stock prices for Google Inc, used to train a model and predict future stock prices as shown below.



For improved predictions, you can train this model on stock price data for more companies in the same sector, region, subsidiaries, etc. Sentiment analysis of the web, news, and social media may also be useful in your predictions. The open-source developer Sentdex has created a really useful tool for S&P 500 Sentiment Analysis.


**Recurrent Neural Networks:**

As we try to model Machine Learning to behave like brains, weights represent long-term memory in the Temporal Lobe. Recognition of patterns and images is done by the Occipital Lobe which works similar to Convolution Neural Networks. Recurrent Neural Networks are like short-term memory which remembers recent memory and can create context similar to the Frontal Lobe. The Parietal Lobe is responsible for spacial recognition like Botlzman Machines. Recurrent Neural Networks connect neurons to themselves through time, creating a feedback loop that preserves short-term and long-term memory awareness.


The following diagram represents the old-school way to describe RNNs, which shows a Feedback Loop (temporal loop) structure that connects hidden layers to themselves and the output layer which gives them a short-term memory.

**Expanded Form Representation:**

A more modern representation shows the following RNN types and use examples:

1.One-To-Many: Computer description of an image. CNN used to classify images and then RNN used to make sense of images and generate context.

2.Many-To-One: Sentiment Analysis of text (gague the positivity or negativity of text)

3.Many-to-Many: Google translate of language who's vocabulary changes based on the gender of the subject. Also subtitling of a movie.


**RNN Gradient Problem:**

The gradient is used to update the weights in an RNN by looking back a certain number of user defined steps. The lower the gradient, the harder it is to update the weights (vanishing gradient) of nodes further back in time. Especially because previous layers are used as inputs for future layers. This means old neurons are training much slower that more current neurons. It's like a domino effect.



Expanding Gradient Solutions
1. Truncated Back-propagation
Stop back-propagation after a certain point (not an optimal because not updating all the weights). Better than doing nothing which can produce an irrelevant network.

2. Penalties
The gradient can be penalized and artificially reduced.

3. Gradient Clipping
A maximum limit for the gradient which stops it from rising more.
