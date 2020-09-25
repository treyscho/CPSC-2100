# CPSC-2100
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
