# ECE2112 Programming Assignment 1

## Table of Contents
### Alphabet Soup Problem: https://github.com/eltonching88/ECE2112-Projects?tab=readme-ov-file#alphabet-soup-problem-1
### Emoticon Problem: (link)
### Unpacking List Problem

## Alphabet Soup Problem
## 1. Define
    '''
    def alphabet_soup(word):
        # Convert to lowercase and sort the list
        letters = list(word.lower())
        letters.sort()
    '''
## 2. 
    
    # Output as string from list
    new = ""
    for i in letters:
        new += i
    return new
## 3.
    # User input
    word = input("Enter a word: ")
    alphabet_soup(word)
