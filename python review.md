# TEST REVIEW
Here are all the questions and solutions for the review
```
#!/usr/bin/env python3

def q1(floatstr):
    '''
    TLO: 112-SCRPY002, LSA 3,4
    Given the floatstr, which is a comma separated string of
    floats, return a list with each of the floats in the 
    argument as elements in the list.
    '''
    return [float(i) for i in floatstr.split(',')]

def q2(*args):
    '''
    TLO: 112-SCRPY006, LSA 3
    TLO: 112-SCRPY007, LSA 4
    Given the variable length argument list, return the average
    of all the arguments as a float
    '''
    return sum(args) / len(args)

def q3(lst,n):
    '''
    TLO: 112-SCRPY004, LSA 3
    Given a list (lst) and a number of items (n), return a new 
    list containing the last n entries in lst.
    '''
    return [i for i in lst[-n:]]
    
def q4(strng):
    '''
    TLO: 112-SCRPY004, LSA 1,2
    TLO: 112-SCRPY006, LSA 3
    Given an input string, return a list containing the ordinal numbers of 
    each character in the string in the order found in the input string.
    '''
    return [ord(i) for i in strng] 

def q5(strng):
    '''
    TLO: 112-SCRPY002, LSA 1,3
    TLO: 112-SCRPY004, LSA 2
    Given an input string, return a tuple with each element in the tuple
    containing a single word from the input string in order.
    '''
    return tuple([i for i in strng.split(' ')])

def q6(catalog, order):
    '''
    TLO: 112-SCRPY007, LSA 2
    Given a dictionary (catalog) whose keys are product names and values are product
    prices per unit and a list of tuples (order) of product names and quantities,
    compute and return the total value of the order.

    Example catalog:
    {
        'AMD Ryzen 5 5600X': 289.99,
        'Intel Core i9-9900K': 363.50,
        'AMD Ryzen 9 5900X': 569.99
    }

    Example order:
    [
        ('AMD Ryzen 5 5600X', 5), 
        ('Intel Core i9-9900K', 3)
    ]

    Example result:
    2540.45 

    How the above result was computed:
    (289.99 * 5) + (363.50 * 3)
    '''
    return sum(catalog[i[0]] * i[1] for i in order)

def q7(filename):
    '''
    TLO: 112-SCRPY005, LSA 1
    Given a filename, open the file and return the length of the first line 
    in the file excluding the line terminator.
    '''
    with open(filename) as filen:
        return len(filen.readline()) - 1

def q8(filename,lst):
    '''
    TLO: 112-SCRPY003, LSA 1
    TLO: 112-SCRPY004, LSA 1,2
    TLO: 112-SCRPY005, LSA 1
    Given a filename and a list, write each entry from the list to the file
    on separate lines until a case-insensitive entry of "stop" is found in 
    the list. If "stop" is not found in the list, write the entire list to 
    the file on separate lines.
    '''
    with open(filename, 'w') as listicle:
        for item in lst:
            if item == 'stop':
                break
            else:
                listicle.write(item + '\n')

def q9(miltime):
    '''
    TLO: 112-SCRPY003, LSA 1
    Given the military time in the argument miltime, return a string 
    containing the greeting of the day.
    0300-1159 "Good Morning"
    1200-1559 "Good Afternoon"
    1600-2059 "Good Evening"
    2100-0259 "Good Night"
    '''
    if miltime < 300 or miltime > 2100:
        return "Good Night"
    elif miltime < 1200:
        return "Good Morning"
    elif miltime < 1600:
        return "Good Afternoon"
    else:
        return "Good Evening"
    
def q10(numlist):
    '''
    TLO: 112-SCRPY003, LSA 1
    TLO: 112-SCRPY004, LSA 1
    Given the argument numlist as a list of numbers, return True if all 
    numbers in the list are NOT negative. If any numbers in the list are
    negative, return False.
    '''
    for num in numlist:
        if num < 0:
            return False
    return True
```
