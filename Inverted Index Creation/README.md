# Inverted Index Creation

## Summary
This project involves creating an inverted index for words and selected bigrams from a collection of text files. You will process the files to generate two outputs:

1. Unigram Index: A file named `unigram_index.txt` containing an inverted index for unigrams.
2. Bigram Index: A file named `selected_bigram_index.txt` containing an inverted index for specific bigrams.

Description
You will work with two datasets:

- devdata: Contains 5 text files for development and testing.
- fulldata: Contains 74 text files for production.

Input Format
Each text file contains key-value pairs in the format:
```
docID \t document_content
```

### Processing Steps
1. Data Cleaning:
   - Replace all punctuation and numerals with spaces.
   - Convert all words to lowercase.
   - Handle `\t` separators in the input files.

2. Unigram Index:
   - Modify the mapper to output `(word, docID)` pairs.
   - Use a HashMap in the reducer to collect and store the inverted index.

3. Bigram Index:
   - Modify the mapper to output `(word1 word2, docID)` pairs for selected bigrams:
     - `computer science`
     - `information retrieval`
     - `power politics`
     - `los angeles`
     - `bruce willis`
   - No changes are required in the reducer.

### Output Format
- Unigram Index: A text file `unigram_index.txt` containing the inverted index for unigrams.
- Bigram Index: A text file `selected_bigram_index.txt` containing the inverted index for the specified bigrams.

## Execution
The task will be performed using a simplified MapReduce setup:
- Fork the example [HadoopWordCounter](https://replit.com/@satychary/HadoopWordCounter) on Replit.
- Modify the provided WordCount code to suit the requirements for unigrams and bigrams.

## Development Tips
- Use the `devdata` collection for testing and debugging.
- Switch to the `fulldata` collection for production.
- To speed up execution, shorten the input files by reducing the number of words (optional).

## Deliverables
1. Output Files:
   - `unigram_index.txt`
   - `selected_bigram_index.txt`
2. Screenshots:
   - Output folder after running the unigram job.
   - Output folder after running the bigram job.
3. Source Code:
   - Mapper and Reducer for unigrams.
   - Mapper for bigrams.


