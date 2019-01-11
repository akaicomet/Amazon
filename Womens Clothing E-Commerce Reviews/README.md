# NLP Feature Engineering 

It quantifies free comment data “Review Text” in Amazon Women Clothing Shopping Review Comment. Comment data like this is said to be an unstructured data. It is not easily be used for traditional analytics. In order to include such a data for our predictive analysis, 5 new numeric metrics are generated from parsing “Review Text”. Quantified “Review Text” metric now can be included in predictive model along with traditional data such as sales data. Keyword Count Percentage is calculated to represent nature of a 'Review Text'. Another calculation is based on Python “Vader Polarity Scores”. 

## Keyword Count
Exclude “Stop Word” such as “is” and “the” and symbols to count keyword. Calculate percentage of word occurrence over total keyword count. For example “love” is 0.002345. “buy” is 0.0001578. Sum all keywords percentage in a “Review Text” entry field and defines the sum of percentage as in new field “GrandTotalProp”. “TotalProp” is a subcategory version of “GrandTotalProp”. Its percentage calculation is based on item category such as “Dress” and “Pants”

## Vader Polarity Scores
This is great Python Sentimental Analysis Package to give a positive, neutral and negative scores from free text data. According to Calderon[2017], “Lexical approaches aim to map words to sentiment by building a lexicon or a ‘dictionary of sentiment.’ We can use this dictionary to assess the sentiment of phrases and sentences, without the need of looking at anything else. Sentiment can be categorical – such as {negative, neutral, positive} – or it can be numerical – like a range of intensities or scores. Lexical approaches look at the sentiment category or score of each word in the sentence and decide what the sentiment category or score of the whole sentence is. The power of lexical approaches lies in the fact that we do not need to train a model using labeled data, since we have everything we need to assess the sentiment of sentences in the dictionary of emotions.”

# Sample
|id|Review Text|GrandTotalProp|TotalProp|compound|neg|neu|pos|
|:-----------|:-----------|:-----------|:-----------|:-----------|:-----------|:-----------|:-----------|    
|0|Absolutely wonderful - silky and sexy and comf...|0.013793|	0.022659|	0.8932|	0.000|	0.272|	0.728|
|1|Love this dress! it's sooo pretty. i happene...  |0.172093|	0.272147|	0.9729|	0.000|	0.664|	0.336|
|2|I had such high hopes for this dress and reall...|0.178479|	0.252226|	0.9427|	0.027|	0.792|	0.181|
|3|I love, love, love this jumpsuit. it's fun, fl...|0.090387|	0.107672|	0.5727|	0.226|	0.340|	0.434|
|4|This shirt is very flattering to all due to th...|0.098637|	0.105174|	0.9291|	0.000|	0.700|	0.300|

# Reference:
Calderon, Pio. 2017, April 10. “VADER Sentiment Analysis Explained”. Retrieved from http://datameetsmedia.com/vader-sentiment-analysis-explained/
		 
