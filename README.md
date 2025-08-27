# ECE2112-Projects

# 1. ALPHABET SOUP PROBLEM
def alphabet_soup(word):
    # Convert to lowercase and sort the list
    letters = list(word.lower())
    letters.sort()

    # Output as string from list
    new = ""
    for i in letters:
        new += i
    return new

# User input
word = input("Enter a word: ")
alphabet_soup(word)
