# ECE2112 Programming Assignment 1 (Python)

## Table of Contents
### 1. [Alphabet Soup Problem](https://github.com/eltonching88/ECE2112-Projects?tab=readme-ov-file#alphabet-soup-problem)
### 2. [Emoticon Problem]()
### 3. [Unpacking List Problem]()

# Section Heading

Some body text of this section.

<a name="my-custom-anchor-point"></a>
Some text I want to provide a direct link to, but which doesn't have its own heading.

(… more content…)

[A link to that custom anchor](#my-custom-anchor-point)


## **Alphabet Soup Problem**
* Create a function that takes a string and returns a string with its letters in alphabetical order.
* 
Step 1. I defined the function `alphabet_soup` to convert all characters in the list `letters` to lowercase and sort the characters
``` python
def alphabet_soup(word):
    # Convert to lowercase and sort the list
    letters = list(word.lower())
    letters.sort()
```
Step 2. I created a string 'new' to store the arranged letters then used for loop to insert the letters to the string
``` python
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
