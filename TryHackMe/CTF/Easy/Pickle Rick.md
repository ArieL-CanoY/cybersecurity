Pinging the ip address, we could know if we can reach the machine and if our vpn through the vpn of tryhackme works

![[Pasted image 20220906180650.png]]



Using nmap, you can see that the ip address that has a services running on port 22 and 80

![[Pasted image 20220906181218.png]]



Port 80 is known for web server, visiting it will show pickle rick page

![[Pasted image 20220906181325.png]]



Visiting the developer tools/inspect element and looking at the code, you will see the username on the body inside the comment

![[Pasted image 20220906181413.png]]



Visiting the robots.txt, you will see random text and that is the password for that username. In simplest explanation, robot.txt is the file that a robot/agent or program that index(search) files and directories on the internet from the public network(especially websites) in order for a user to find it on the search engines result. If a user search for your domain or ip address with files or directories name, the search engines like google will show a result.

![[Pasted image 20220906181619.png]]



Using tools like dirbuster, you will see different directories and one of them is login.php

![[Pasted image 20220906182337.png]]



Visiting the login.php directory will show up login page, putting the valid credentials will let you in the portal.php that you can type linux command

![[Pasted image 20220906182538.png]]



Type whoami to see who we are running on the machine and we can see that we are www-data 

![[Pasted image 20220906184926.png]]



Printing the list of files and directories of current directory and you will see the filename named "Sup3rS3cretPickl3Ingred.txt" which is the first flag for this room

![[Pasted image 20220906182744.png]]



Using cat command to concatenate the output to the website will say that the command is disabled for future pickle rick

![[Pasted image 20220906182815.png]]



Searching for alternative commands for cat, you will see the command tac which is also same feature as cat command.

![[Pasted image 20220906183129.png]]



 Using tac, we can output the text file that we want , so we can use it on the text file supersecretingredients.txt which is the first flag

![[Pasted image 20220906183209.png]]

![[Pasted image 20220906183236.png]]


 To find the second flag, there is a clue.txt file on the current directory which tell to us to look around to the other directories and there is a text file on the home directory of rick which is on /home/rick/second ingredients and using file command, we can see that it is an ascii file, use tac to reveal the flag. Remember that a file or directory with space should use single or double qoute like this: tac /home/rick/'second ingredients'

![[Pasted image 20220906183539.png]]

![[Pasted image 20220906184625.png]]

![[Pasted image 20220906184217.png]]

![[Pasted image 20220906184648.png]]



To find the last/third flag, there is possibility that it is always on the root home directory, but we cannot see the files when we use ls /root because we are only www-data user and we are not root, and as you can see on the file permission, only root and has sudo/root privilege user can access the file. 

![[Pasted image 20220906185041.png]]



Typing "sudo -l" will show what commands you can run with the current user, and you can see that you can run any commands without asking the password of current user

![[Pasted image 20220906182643.png]]



We can run sudo ls /root to see the file (if it has the last/third flag)

![[Pasted image 20220906191013.png]]



	Using sudo tac /root/3rd.txt will reveal the flag

![[Pasted image 20220906191404.png]]

![[Pasted image 20220906191423.png]]

