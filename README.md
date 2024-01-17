# Public-library


## About this idea

- In fact, this idea came from a news article I read during my college days, which reported that China had opened public libraries in some poor areas and listed a list of screened books, but I felt a little bit regretful that all the books were in Chinese, I don't mean to say that this is a bad behavior, but I would like to bring some books in English to the people in poor areas, including the children, to broaden their horizons more. I would like to bring some English books to people in poor areas, including children, so as to broaden their horizons. So the purpose of this program is to select 100 to 200 English books that are less difficult to read, affordable, and have high ratings, and I hope I can really contribute to the world by donating these books in the future!


## Goals

Filter the dataset of English-language books for 100 to 200 books that fit the criteria.

***

## DataSets

###

| NO. | Date | Data | Source | Additional instructions
| :---: | :---: | :--- | :--- | :---|
| 1 | `2024-01-09` | [The dataset of Goodreads](books_1.Best_Books_Ever.csv) | [Google Dataset Search](https://doi.org/10.5281/zenodo.4265096)|
| 2 | `2024-01-16` | [The dataset of Lexile](Lexile_score.csv) | My original  | [Introduction to Lexile](https://en.wikipedia.org/wiki/Lexile)


***  

## Project packages 

The python packages included in this program include pandas, re, matplotlib, seaborn, ast, and counter.

***

## Description of the purpose of the program
1.First I started by downloading the data I found from the Google dataset (books_1.Best_Books_Ever.csv) into Googlecolab to read it and store it (books_df)

2.Secondly, my purpose this time is to filter out English books, so I use foreign_language_books_df to store the filtered results.

3.Then, since the main target this time was children, some keywords were filtered for use in the filtering, which was used to ensure that the genre of the book did not contain these factors ('Mature', 'Violence', 'Sexual', 'Explicit', 'Horror')

4.After this, it is also important to filter the books for positive reviews, reads, and scores(rating(>=4.0) and enough people commented(>=200000) and  a high enough positive rating(>=95.0), which demonstrate the quality as well as the popularity of the book.

5.Finally, given the cost factor, we need to filter for books that are best priced below $20(affordable_books)

6.On the basis of the previous screening of more than 30,000 books to only 165 books, but also need to consider is the difficulty of reading books to match, so I began to look for books about the difficulty of reading the dataset, I found through browsing in some parts of the United States will be used to Lexile standards for classification of books, through the ratings to show the difficulty of reading, but it is a great pity that I did not find the appropriate In order to make sure the results are more accurate, I copied the titles of the 165 books I found and searched for the corresponding scores one by one on the Lexile website and created a new file to record the scores (Lexile_score.csv). Because there are some books that are not rated on the Lexile website, I've set their ratings to NaN for the sake of caution.

7.In the end I filtered out 114 books, which is considered to be the desired goal, after that it was the visualization stage, through the analysis I visualized the ten most read books, the ten most popular book genres, the average ratings of the ten best-selling authors (this data only), the number of book counterparts and their ratings, the price trend of the books, and the ratings versus the number of reads.

***
## Apologize

This is my first time to use and upload the file to Github, may be due to the use of the lack of proficiency and lead to some problems, I hope that both students or teachers to find problems in the program can be kindly pointed out, I will be seriously modified and hope to be able to share and exchange with more people to write the program experience. Many thanks.
