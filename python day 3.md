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
