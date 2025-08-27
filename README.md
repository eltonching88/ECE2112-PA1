# ECE2112 Programming Assignment 1 (Python)

## Table of Contents
### 1. [Alphabet Soup Problem](#anchor-alphabet_soup)
### 2. [Emoticon Problem](#anchor-emoticon)
### 3. [Unpacking List Problem](#anchor-unpacking_list)


<a name="anchor-alphabet_soup"></a>
## **Alphabet Soup Problem**
* Create a function that takes a string and returns a string with its letters in alphabetical order

**Step 1.** I defined the function `alphabet_soup(word)`, which converts all characters in the list `letters` to lowercase and sort the characters
``` python
def alphabet_soup(word):
    # Convert to lowercase and sort the list
    letters = list(word.lower())
    letters.sort()
```
<br/>

**Step 2.** I created a string `new` to store the arranged letters, then used a for loop to insert the letters into the string
``` python
# Output as string from list
new = ""
for i in letters:
    new += i
return new
```
<br/>

**Step 3.** The user can enter any string, then the input `word` will be put in the function `alphabet_soup()` 
> [!NOTE]
> I used the same variable name for the input `word` and function `alphabet_soup(word)` to avoid confusion

``` python
# User input
word = input("Enter a word: ")
alphabet_soup(word)
```
<br/>

**Expected Output**: 
``` python
'Hello' >> 'ehllo'
```

<br/>


<a name="anchor-emoticon"></a>
## **Emoticon Problem**
* Create a function that changes specific words into emoticons. Given a sentence as a string, replace the words smile, grin, sad and mad with their corresponding emoticon

**Step 1.** The function `emotify(text)` contains a dictionary `emojis` that has keys-values for each of the given emojis. I looped the key `word` and value `emoji` in the dictionary to iterate each item and replace the user input `text` of similar keys with their value. Using text.replace(), I accounted for 3 cases: (1) same case, (2) all uppercase, and (3) all lowercase.
> [!NOTE]
> I did not account for other cases, such as input `SMile` since this would be grammatically incorrect.

``` python
def emotify(text):
    # Dictionary of emojis
    emojis = {"Smile":":)", "Grin":":D", "Sad":":((", "Mad":">:("}
    
    for word, emoji in emojis.items():
        text = text.replace(word, emoji)         # Smile to :)
        text = text.replace(word.upper(), emoji) # SMILE to :)
        text = text.replace(word.lower(), emoji) # smile to :)   
        
    return text
```
<br/>

**Step 2.** I created a string `new` to store the arranged letters, then used a for loop to insert the letters into the string
``` python

```
<br/>

**Step 3.** The user can enter any string, then the input `word` will be put in the function `alphabet_soup()` 
> [!NOTE]
> I used the same variable name for the input `word` and function `alphabet_soup(word)` to avoid confusion
``` python

```
<br/>

**Expected Output**: 
``` python
'Hello' >> 'ehllo'
```

<br/>


<a name="anchor-unpacking_list"></a>
## **Unpacking List Problem**
* Create a 

**Step 1.** I defined the function `alphabet_soup` to convert all characters in the list `letters` to lowercase and sort the characters
``` python

```
<br/>

**Step 2.** I created a string `new` to store the arranged letters, then used a for loop to insert the letters into the string
``` python

```
<br/>

**Step 3.** The user can enter any string, then the input `word` will be put in the function `alphabet_soup()` 
> [!NOTE]
> I used the same variable name for the input `word` and function `alphabet_soup(word)` to avoid confusion
``` python

```
<br/>

**Expected Output**: 
``` python
'Hello' >> 'ehllo'
```

<br/>
