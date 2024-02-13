```python
import os

os.getcwd()                                    #return current working directory
os.chdir('C:\\Users\User1\Downloads')       #change directory - can be absolute or traversing like ../../
os.listdir(os.cwd())                          #list files in that path, can be specify
os.mkdir("Folder1")
os.makedirs("Folder1/Folder1v1")
os.rmdir('Folder1')
os.path.isfile(os.listdir(os.getcwd())[index])
file = open('text1.txt', 'w')
	file.write('score = 1212')
	file.close()
os.path.join(directory, file)
os.walk()
os.path.basename('/Desktop/sample.txt')           #return sample.txt
os.path.dirname('/Desktop/sample.txt')          #return /Desktop
os.path.exist(file)
os.path.isdir(file)
os.path.isfile(file)
os.path.splitext('/Desktop/sample.txt')           #return ('/Desktop/sample', '.txt')
os.stat('file')
os.system('dir')  # execute a command from the OS
```




list all files including files from subfolders
```python
# using os.walk(directory)

import os


fileList = os.walk(os.getcwd())  
  
for root, folderName, files in fileList:  
    print(f'root: {root}')  
    for file in files:  
        print(f'------- {file}')  
        namesCount += 1

```