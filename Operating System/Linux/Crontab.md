```python
crotab -l   - show the current user's cron jobs
crontab -e   - edit the crontab jobs

parts:
	min    hr    day of month    month    day of week  command

ex. 
	* * * * * echo 'another text' >> /home/user/crontab.txt
		- meaning, run this every minute, every hour, every day, every month, every week

	<options> command 
		- execute command when some time or process happened
		options:
			@hourly - run every start of an hour
			@daily - run every start of a day - 12:00 am
			@monthly - run every start of a month
			@reboot - run after system reboot
	crontab -u <user> -e
		- execute command on behalf of specific user
		- if no -u <user> specified then the current user will use
		


config files      
	/etc/crontab


directory of config files
	/etc/
	/etc/cron.daily
	/etc/cron.hourly
	/etc/cron.monthly
	/etc/cron.weekly
	

```









