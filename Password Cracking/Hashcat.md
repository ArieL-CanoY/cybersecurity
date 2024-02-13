password recovery tool that use for password attack such as brute force and dictionary attacks

```bash
hashcat [options] [hash/hash list] [password list]

-m          - type of hash mode
  
	  900 | md4
	    0 | md5
	  100 | sha1
	 1000 | NTLM
	   23 | Skype
	11600 | 7-Zip
   
	and	many more



-a          - type of attack mode. Straight for passwordlist, bruteforce for all combinations

	0 | Straight
	1 | Combination
	3 | Brute-force
	6 | Hybrid Wordlist + Mask
	7 | Hybrid Mask + Wordlist
	9 | Association



-D          - device type to choose for cracking the password (default is CPU). 1 for CPU, 2 for GPU


--show      - show the password cracked



sample commands:

	With password list:
	    
	    hashcat -m 0 -a 0 hash.txt /usr/share/wordlists/password-list/rockyou.txt --status --show

  

    brute-forcing password from a-z,A-z,0-9,all symbols

	    hashcat -m 0 -a 3 hash --status -D 1,2 ?a?a?a?a?a?a?a?a?a?a?a --increment


  

-------------------- Other --------------------

#convert string to md5

echo -n [STRING] | md5sum | tr -d '  -' > hash.txt
```