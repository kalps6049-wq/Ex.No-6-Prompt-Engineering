Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

Aim: 

Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools.

Explanation:

Develop a python code that integrates multiple AI tool by interacting with their APIs.
Compare outputs from different APIs.
Analyze the response and the Output.

The aim is to understand how to request help from AI tools for tasks like writing Python code, integrating with APIs, comparing outputs, and generating actionable insights.

PROCEDURE:

 1.Install the required Python libraries such as NLTK.


2.Import the necessary modules for sentiment analysis.


3.Download the required dataset (VADER lexicon) used for analyzing sentiment.


4.Generate sample AI text that simulates responses produced by different AI tools.


5.Display the generated text.


6.Use the VADER Sentiment Analyzer to analyze the sentiment of the generated text.


7.Calculate sentiment scores such as positive, negative, neutral, and compound values.


8.Interpret the compound score to determine whether the text sentiment is positive, negative, or neutral.


9.Display the insight based on the sentiment result.


POSITIVE CODE:
```

from nltk.sentiment import SentimentIntensityAnalyzer
import nltk

nltk.download('vader_lexicon')

# Simulated AI-generated text
generated_text = "This smartphone offers outstanding battery life and an intelligent AI camera that captures stunning photos."

print("Generated Review:\n")
print(generated_text)

# Sentiment analysis
sia = SentimentIntensityAnalyzer()
sentiment = sia.polarity_scores(generated_text)

print("\nSentiment Analysis:")
print(sentiment)

# Insight generation
if sentiment['compound'] > 0:
    print("\nInsight: The review is positive and suitable for marketing promotion.")
else:
    print("\nInsight: The review tone is neutral or negative.")
```

OUTPUT:

This smartphone offers outstanding battery life and an intelligent AI camera that captures stunning photos.

Sentiment Analysis:
{'neg': 0.0, 'neu': 0.556, 'pos': 0.444, 'compound': 0.8625}

Insight: The review is positive and suitable for marketing promotion.

NEGATIVE CODE:
```

from nltk.sentiment import SentimentIntensityAnalyzer
import nltk

nltk.download('vader_lexicon')

# Simulated AI-generated negative text
generated_text = "This smartphone has terrible battery life and the camera quality is very poor."

print("Generated Review:\n")
print(generated_text)

# Sentiment analysis
sia = SentimentIntensityAnalyzer()
sentiment = sia.polarity_scores(generated_text)

print("\nSentiment Analysis:")
print(sentiment)

# Insight generation
if sentiment['compound'] > 0:
    print("\nInsight: The review is positive and suitable for marketing promotion.")
else:
    print("\nInsight: The review tone is neutral or negative.")
```

OUTPUT:

This smartphone has terrible battery life and the camera quality is very poor.

Sentiment Analysis:
{'neg': 0.371, 'neu': 0.629, 'pos': 0.0, 'compound': -0.7574}

Insight: The review tone is neutral or negative.

RESULT:
The Python program was successfully developed and executed. The generated AI text was analyzed using sentiment analysis, and the program correctly identified whether the text was positive, negative, or neutral based on the compound sentiment score. The code demonstrated compatibility with multiple AI-generated text outputs.







