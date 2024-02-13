```python
crontab -e   - edit the crontab jobs

parts:
	min    hr    day of month    month    day of week  command

ex. 
	* * * * * echo 'another text' >> /home/user/crontab.txt
		- meaning, run this every minute, every hour, every day, every month, every week


config files      
	/etc/crontab


directory of config files
	/etc/
	/etc/cron.daily
	/etc/cron.hourly
	/etc/cron.monthly
	/etc/cron.weekly
	

```









