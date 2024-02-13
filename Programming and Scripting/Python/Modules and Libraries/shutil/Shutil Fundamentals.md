```python
# source and destination should be a file, and it can have a directory from other directory/folder source or destination


shutil.move('source', 'destination')

	#best way to concatenate file and directory 
	#example
	fromDirectory = 'C:\\Users\Asus-pc\Downloads\MP3 Files'
	fromFilename = 'Adie - Mahika.mp3'
	fromDirWithFile = fromDirectory + '\\' + fromFilename

	toDirectory = 'C:\\Users\Asus-pc\Downloads\MP3 Files\Adie'
	toFilename = 'adie - mahika.mp3'
	toDirWithFile = toDirectory + '\\' + toFilename
	shutil.move(fromDirWithFile, toDirWithFile)

```