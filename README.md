# SentimentOfFakeNewsData

The code and data repository for the paper "On Sentiment of Online Fake News"

# Structure of this repository:

## readme.txt: 

This readme file.

## DataInputs: 

Seven datasets collected from the literature and cleaned up to include only statements and their truth labels. 

In an effort for consistency, we kept the truth labels exactly the same as the original datasets.

For the TVS-U dataset: 1:"Satire", 2:"Hoax", 3:"Propaganda", 4:"Trusted"

For the TVS-P dataset: Truth-Ratings are listed as integers from 0-5 (0 is True, 5 is Pants-on-Fire). Note that TVS-P is effectively a subset of the Liar dataset, so we do not report its results in the paper.

## TextBlob_Senti_Ana.ipynb and AFFIN_Senti_Ana.ipynb: 

Jupiter Notebooks containing code to extract the sentiment of statements in the above data input files, for the TextBlob and AFINN tools using Python. To obtain sentiments from the MeaningCloud tool, one should download and install the Excel add-in of MeaningCloud at https://www.meaningcloud.com/developer/excel-addin and run it on the input Excel files.

## MeaningCloud_Output: 

MeaningCloud sentiments created with MeaningCloud Excel add-in. File names indicate dataset files and sentiment extraction tools: dataset-tool.txt
  
## TextBlob_Output: 

TextBlob sentiments created with the Python scripts provided. File names indicate dataset files and sentiment extraction tools: dataset-tool.txt
  
## AFINN_Output: 

AFINN sentiments created with the Python scripts provided. File names indicate dataset files and sentiment extraction tools: dataset-tool.txt
  
## SPSS: 

IBM SPSS outputs of statistical significance and gamma calculation. 

Truth labels: In each dataset, we have the truth value replaced with an ordinal value.  In detests that have only false and true labels, we show (in the SPSS files) 0 for false and 1 for true. In datasets with 6 levels of truth, six ordinal values are used. 

Sentiment categories: In order to avoid excessive renaming of sentiment values but impose the order between them (i.e., N+<N<NEU<P<P+) we have replaced N+ with A or AN+. The rest of the sentiment categories accidentally fell in order when ordered alphabetically by SPSS. In other words, when sorted alphabetically, A (AN+)<N<NEU<P<P+.

None values produced by MeaningCloud are treated as missing.



