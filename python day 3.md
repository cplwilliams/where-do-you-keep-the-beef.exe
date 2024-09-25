# Python Day 3
## File I/O
This is a way to open a file in read mode
```
with open("test.txt") as fp:
  pass
```
In order to open a file in write mode, you have to be more explicit. You have to add `'w'` when opening the file. 
Writing the file you use the object you created in the first line with fuction `.write()` this writes whatever you put into the file
`.writelines()` writes multiple lines at once to a file. If you have a list, like in this example it makes it pretty easy.
```
with open('test.txt', 'w') as fp:
    fp.write('First line\n')
    lines = ['Second line\n', 'Third line\n', 'Fourth line\n', 'Last line\n']
    fp.writelines(lines)
```
this is what I used to complete the last thing on this website:

[[https://runestone.academy/ns/books/published/fopp/Files/ChapterAssessment.html]]
```
with open('SP500.txt') as stonk:
    avgList = []
    max_interest = 0.0
    for line in stonk:
        linelist = line.split(',')
        if linelist[0] == 'Date':
            continue
        datesplit = linelist[0].split('/')
        if int(datesplit[2]) > 2017 or int(datesplit[2]) < 2016:
            continue
        elif int(datesplit[2]) == 2017 and int(datesplit[0]) > 5:
            continue
        elif int(datesplit[2]) == 2016 and int(datesplit[0]) < 6:  
            continue
        avgList.append(float(linelist[1]))
        if float(linelist[5]) > max_interest:
            max_interest = float(linelist[5])
    mean_SP = sum(avgList) / len(avgList)
```
