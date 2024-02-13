Compressing and decompressing using terminal is good when you have only terminal on your screen and this is good for remote access
#### tar
```bash
-c - create - use when creating tar file

-f - file - specify that the it will archive file

	ex: tar -cf [filename to create for tar after compression] [filename to compress]

-x - extract 

	ex: tar -xf [filename to create for tar after compression] [filename to compress]
	
-v - verbose - add information about the file being compress or decompress



```



#### gzip
```bash
Compressing

	gzip [filename] - compress the file and removing the original file

-k - keep the original file


When using tar command:

-cfxv - same as the above

-z - use to specify that it will compress to gzip/gunzip

	ex: tar czf [filename to create for tar after compression] [filename to compress] - use when compressing
	
	tar -zxvf [filename to decompressed] - use when decompressing
```


# zip
```python
definition: package and compress (archive) files


zip [zip filename] [files can file1 file2 file3]   - zip the files



unzip -l [zip filename]  - show the list of files or folders in the zip filename




```













