# AC3.2-Frankentable

# Object

Build a TableView based app that parses a block of text and displays a concordance of 
Mary Wollstonecraft (Godwin) Shelley's **Frankenstein** in a table. Each row of the table should display a
unique word in it and its frequency count next to it. 

# Steps

1. The usual forking and cloning. This time there is a project inside named Frankentable.
  Open it.
2. The project has a Table View controller and a Data.txt file with a small excerpt from the book. 
  This file is opened and spat out in viewDidLoad to get you going.
3. Split the block of text into unique words and count their frequency. Probably going to want 
  to use a Dictionary.
4. Display one row per word, showing the word and its frequency,
  Example cell:
  
    ```
    ***********************************
    *                                 *
    *   Albatross (12)                *
    *                                 *
    ***********************************
    ```
  
5. Sort alphabetically, with a section for each letter of the alphabet, grouping by
  the initial letter of each word.

6. Sort by frequency, ordered reverse. I.e. the most frequent word should be in the
  first cell, the least in the last. Section by distinct freqency counts. For example,
  say the highest frequency was 43 and there was 1 word with that frequency, then a
  section named "43" would have that one row. If the next most frequent word occurred 22 times, and
  there were three such words, they would be in the "22" section.  And so on.

7. Optional: If you feel ambitious you could grab the full data via an web request to http://www.gutenberg.org/cache/epub/84/pg84.txt.
  It would be wrong to call this an API call because it's just a text file. Don't try to turn it
  into JSON. Just read it like we're doing with the local file. It should still be done
  asynchronously.
