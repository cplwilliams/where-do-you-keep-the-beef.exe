# Python Day 1
## split example
```
string splits
email = 'name@domain.com'
a = email.split('@')
b = '.'.join(a)
c = b.split('.')
print(c)
```
## other split example
```
lst= []
a = email.split('@')
b = a[1]/split('.')
lst.append(a[0])
lst.append(b[0])
lst.append(b[1])
print(lst)
```
## my fizzbuzz
```
number = int(input("gimme your digit:"))

if(number % 3 == 0):
    print("fizz", end='')
if(number % 5 == 0):
    print("buzz", end='')
if(not (number % 5 == 0) and not (number % 3 == 0)):
    print(number, end='')
print()
```

##Codewars
https://www.codewars.com/kata/55c45be3b2079eccff00010f/train/python
'''
def order(sentence):
    # code here
    wordList = sentence.split(" ")
    print(wordList)
    orderedWordList = wordList
    if len(wordList) == 0:
        return ""
    for word in wordList:
        for char in word:
            if char.isnumeric():
                orderedWordList[int(char) - 1] = word
    orderedSentence = " ".join(orderedWordList)
    return orderedSentence
'''
