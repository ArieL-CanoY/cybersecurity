
# Definition
```python
- stands for Common Vulnerability Scoring System.
- used to define the severity of a vulnerability based on a numerical score.
- tandardized framework used to assess and communicate the severity of software vulnerabilities. Developed by the Forum of Incident Response and Security Teams (FIRST).
- CVSS provides a way to quantify the risk posed by vulnerabilities, allowing organizations to prioritize their responses effectively.
- the score is between 0 and 10:
	- none: 0.0
	- low: 0.1 - 3.9
	- medium: 4.0 - 6.9
	- high: 7.0 - 8.9
	- critical 9.0 - 10.0
```


# Base metrics
```python
------ Exploitability ------
>> Attack Vector
	- from where the attack can be mounted:
		- network
		- adjacent
		- local
		- physical

>> Attack Complexity
	- conditions outside attacker's control
		- low
		- high

>> Privileges Required
	- access needed to mount an attack
		- none
		- low
		- high

>> User Interaction
	- user involvement to perform an attack
		- none
		- required




------ Impact ------
>> Confidentiality
	- disclosure of data
		- none
		- low
		- high

>> Integrity
	- modification of data
		- none
		- low
		- high

>> Availability
	- denial of accessibility
		- none
		- low
		- high

>> Scope
	- scope of affected component
		- unchanged
		- changed
```



# Temporal metrics
```python
Note: the not defined value is used when there is not sufficient information to set to other values even in unknown.


>> Exploit Code Maturity
	- status of exploit code
		- unproven
		- proof of concept
		- functional
		- high
		- not defined


>> Remediation Level
	- status of patches and updates 
		- official fix
		- temporal fix
		- workaround
		- unavailable
		- not defined


>> Report Confidence
	- certainty of vulnerability root cause
		- unknown
		- reasonable
		- confirmed
		- not defined

Temporal CVSS score <= Base CVSS score
```




# Environmental metrics
```python
- allows organization to customize score in the base score
- can have not defined values just like in temporal metrics if nothing has changed
- 2 types of customization:
	- all metrics of the base score can be modified
	- add requirements for the impact metrics: CIA requirements
		- the requirements can be set to:
			- low
			- medium
			- high
			- not defined
```




# Vectorized Information
```python
>> CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:L/A:N/E:H/RL:U/RC:R/CR:H/MAC:L
	Meaning:
		----- base metrics -----
		AV:N - attack vector: network
		AC:H - attack complexity: high
		PR:N - privileges required: none
		UI:N - user interaction: none
		S:U - scope: unchanged
		C:H - confidentiality: high
		I:L - integrity: low
		A:N - availability: none

		----- temporal metrics -----
		E:H - exploit code maturity: high
		RL:U - remediation level: unavailable
		RC:R - report confidence: reasonable



		----- environmental metrics -----
		CR:H - confidentiality metrics: high
		MAC:L - modified attack complexity: low


note: often you will see base metrics

```




























