# ECE2112 Programming Assignment 1

## Table of Contents
### 1. [Alphabet Soup Problem](https://github.com/eltonching88/ECE2112-Projects?tab=readme-ov-file#alphabet-soup-problem-1)
### 2. [Emoticon Problem]()
### 3. [Unpacking List Problem]()


## **Alphabet Soup Problem**
Step 1. I defined the function 'alphabet_soup' to convert all characters in the list 'letters' to lowercase and sort the characters
```
def alphabet_soup(word):
    # Convert to lowercase and sort the list
    letters = list(word.lower())
    letters.sort()
```
Step 2. I created a string 'new' to store the arranged letters then used for loop to insert the letters to the string
```  
# Output as string from list
new = ""
for i in letters:
    new += i
return new
```
## 3.
    # User input
    word = input("Enter a word: ")
    alphabet_soup(word)
