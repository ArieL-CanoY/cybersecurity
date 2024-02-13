```python
import time

time.time()                # total num of seconds since the beginning 
time.asctime()             # ex. output is Tue Jan 20 12:23:00 2023	

#more managable and readable
	now = time.localtime()  
	print(f'{now.tm_hour}:{now.tm_min}:{now.tm_sec}')  #ex. output is 12:30:1
	

```