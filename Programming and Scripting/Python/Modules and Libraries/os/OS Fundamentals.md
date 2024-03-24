```python
import os


os.getcwd()  #return current working directory
os.chdir('C:\\Users\User1\Downloads')  #change directory - can be absolute or traversing like ../../
os.listdir(os.cwd())  #list files in that path, can be specify
os.mkdir("Folder1")  # make a folder
os.makedirs("Folder1/Folder1v1")  # make multiple folders
os.rmdir('Folder1')  # remove a folder
os.rename('file1', 'newfile1')  # rename a file or directory
os.path.isfile(os.listdir(os.getcwd())[index])  # check if the path is a file based on the list of files from the directory
file = open('text1.txt', 'w')
	file.write('score = 1212')
	file.close()
os.path.join(directory, file)  # easier method to concatenate directory and file which other method can cause an error
os.walk()  # traverse from a folder to different folders and files
os.path.basename('/Desktop/sample.txt')           #return sample.txt
os.path.dirname('/Desktop/sample.txt')          #return /Desktop
os.path.exist(file) # returns a boolean value if the path exist
os.path.isdir(file)  # returns a boolean value if the path is a diretory
os.path.isfile(file)  # returns a boolean value if the path is a file
os.path.split('/Desktop/sample.txt')  #return ('/Desktop/sample', 'sample.txt')
os.path.splitext('/Desktop/sample.txt')  #return ('/Desktop/sample', '.txt')
os.stat('file')  # show details of a file
os.system('dir')  # execute a command from the OS
os.environ  # returns the list of environmental variables set from the current operating system
os.environ.get('<environmental variable key name>')  # returns the value of key of an environmental variable

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