# CPSC-2100
Problem 1.1

def vowels(word):
    numOfVowels = 0;
    for letter in word:
        if letter in ('aeiouAEIOU'):
            numOfVowels = numOfVowels + 1
            print(letter)
    print('Number of vowels: ' + str(numOfVowels))
    
Problem 1.2

def bobs(word):
    iterator = 0;
    numOfBobs = 0;
    while (iterator < len(word)):
        if (word[iterator: (iterator+3)] == 'bob'):
            numOfBobs+=1
        iterator+=1
    print(str(numOfBobs))

Problem 1.3

def longest_alpha(word):
    word.lower();
    longestString = '';
    currentLongestString = '';
    for i in range(len(word)-1):
        if word[i] <= word[i+1]:
            currentLongestString += word[i];
        else:
            if len(currentLongestString) > len(longestString):
                longestString = currentLongestString + word[i];
            currentLongestString = '';
    print('The longest run of the word in alphabetical order is: ' + longestString);
