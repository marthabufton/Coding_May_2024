# Notes June 18 2024

## First part:

## Open file, declare element, cast as variable type that can be read

Step one: export the csv file and save it in the right folder.This folder in this case is Python II
Step two: import the libraries: Pandas and NLTK
Step three: declare variables
  - Variable 1: Declare the Review file as a dataframe so that Pandas as a library knows what to do, which has the tabular data. This data is a column in a table, it is not yet a single block of string so the NLTK can't work with.
    - Review_df = Review_June18.csv #step of conversion because recognized by Pandas (open)
  - Variable 2: The column has to be declared.
    - Review_abstract = Review.df ['Description']
  - Cast the column as a list because this is what is read by the NLTK and identifying location
    - Review_abstract = list(Review_df['Description'])
- Step four: convert the description column ()




- Final solution for the case study of working with a csv file to clean data and do text analysis
  - Inputs (introduction)
     Libraries
        - Pandas: work with tabular data
        - NLTK: analyze the data
    - Variables and files
      - csv file
    - Functions
      - Specify each step

  - Tasks (body paragraphs)
    - counting
    - searching
  - Outputs (conclusion)
    - "Wrangled" list that can be searched


List_of_articles = "LitReview_June18.csv"


Libraries
# Pandas to work with tabular data, i.e., the csv file


# Natural language toolkit for text analysis
import nltk

# tokenization is the process of splitting strings into their individual "tokens"
from nltk.tokenize import word_tokenize, sent_tokenize
from nltk.corpus import stopwords

nltk.download('punkt')
nltk.download('stopwords')

# to import a .txt file we use the "open" function, giving it the path to our text file and an instrution about what we want to do with the file
# here, we would like to "read" our file into a variable so 
transcript = open('Bette-Smith-Transcript.txt').read().lower()

for name in list_of_names:
    # we check if this name includes "Dobson"
    if "Dobson" in name:
        # if this is True, we add this name to our new list
        only_dobsons.append(name)