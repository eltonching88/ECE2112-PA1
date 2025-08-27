# ECE2112 Programming Assignment 1 (Python)

## Table of Contents
### 1. [Alphabet Soup Problem](#anchor-alphabet_soup)
### 2. [Emoticon Problem](#anchor-emoticon)
### 3. [Unpacking List Problem](#anchor-unpacking_list)
<br/>

<a name="anchor-alphabet_soup"></a>
## **Alphabet Soup Problem**
* Create a function that takes a string and returns a string with its letters in alphabetical order.

**Step 1.** I defined the function `alphabet_soup(word)`, which converts all characters in the list `letters` to lowercase and returns the sorted characters.
``` python
def alphabet_soup(word):
    # Convert to lowercase and sort the list
    letters = list(word.lower())
    letters.sort()
```
<br/>

**Step 2.** I created a string `new` to store the arranged letters, then used a for loop to insert the letters into the string.
``` python
# Output as string from list
new = ""
for i in letters:
    new += i
return new
```
<br/>

**Step 3.** The user can enter any string, then the input `word` will be put in the function `alphabet_soup()`.
``` python
# User input
word = input("Enter a word: ")
alphabet_soup(word)
```
> [!NOTE]
> I used the same variable name for the input `word` and function `alphabet_soup(word)` to avoid confusion.
<br/>

**Expected Output**: 
``` python
'Hello' >> 'ehllo'
```

<br/>


<a name="anchor-emoticon"></a>
## **Emoticon Problem**
* Create a function that changes specific words into emoticons. Given a sentence as a string, replace the words smile, grin, sad and mad with their corresponding emoticon.

**Step 1.** The function `emotify(text)` contains a dictionary `emojis` that has keys-values for each given emoji. I looped the key `word` and value `emoji` in the dictionary to iterate each item and replace the user input `text` of similar keys with their value. Using text.replace(), I accounted for 3 cases: (1) same case, (2) all uppercase, and (3) all lowercase.
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
> [!NOTE]
> I did not account for other cases, such as input `SMile`, since this would be grammatically incorrect.
<br/>

**Step 2.** The user can input any sentences, then the function `emotify(txt)` is called.
``` python
# User input
txt = input("Send message: ")
emotify(txt)
```
<br/>

**Expected Output**: 
``` python
'Make me smile, I am MAD.' >> 'Make me :), I am >:(.'
```

<br/>


<a name="anchor-unpacking_list"></a>
## **Unpacking List Problem**
* Unpack the list into three variables, being first, middle, and last, with middle being everything in between the first and last element. Then print all three variables.

**Step 1.** I defined the function `unpack(lst)` to do the following functions. The first and last values can be easily unpacked by assigning the values of the list's index [0] and [-1].
``` python
def unpack(lst):

    # Separate first and last using index 0, -1
    first = (lst[0])
    last = (lst[-1])
```
<br/>

**Step 2.** In the same function, the values in between the first and last loops through the list `lst`. The variable `middle` stores the values as string to output it as part of a text. Then, I store the list's length in `n`. I can now begin the for loop within the range 1 to n-1 since I need to output the second and the second to the last indexes' values. The `value` stores the numbers and adds it to `middle` for each iteration.
``` python
    # Get the value in between
    middle = ""

    n = len(lst)
    for i in range(1,n-1): # [1,(2),(3),(4),(5),6]
        value = (lst[i])
        middle += str(value)
        if i < n-2: 
            middle += ", "
 ```
> [!NOTE]
> The if statement is optional and only makes the output readable.
<br/>

**Step 3.** In the same function, I simply print the output for each variable and return to the main function.
``` python
    print("First:\t" + str(first))
    print("Middle:\t[" + middle + "]")
    print("Last:\t" + str(last))

    return 
```
<br/>

**Step 4.** In the main function, I created two sample lists to call the function and output the unpacked lists accordingly.
``` python
lst = [1,2,3,4,5,6]
unpack(lst)

lst = [1,2,3,4,5,6,7,8]
unpack(lst)
```
<br/>

**Expected Output**: 
``` python
First:	1
Middle:	[2, 3, 4, 5]
Last:	6
First:	1
Middle:	[2, 3, 4, 5, 6, 7]
Last:	8
```

<br/>

**Alternate Solution.** This uses the concept of unpacking a tuple.

**Step 1.** In the function `unpack(lst)`, I assigned three variables to the list `lst` and used an asterisk `*` with `middle`. The asterisk assigns the values without a specific variable. Since there are only three variables, `first` is assigned to index [0] and all other indexes are assigned to `middle` except for the last index since we introduced a third variable. 

``` python
def unpack(lst):

    # OPTION 2: Using list unpacking
    first, *middle, last = lst
    
    print("First:\t", first)
    print("Middle:\t", middle)
    print("Last:\t", last)
    
    return 
```
> [!NOTE]
> The `first, *middle, last = lst` is a simpler code that can be found in w3schools.com.
<br/>

**Step 2.** The main function provides the given list to the function and the returned values are automatically formatted similar to the example in the module.
``` python
lst = [1,2,3,4,5,6]
unpack(lst)
```
<br/>

**Expected Output**: 
``` python
First:	 1
Middle:	 [2, 3, 4, 5]
Last:	 6
```

<br/>

