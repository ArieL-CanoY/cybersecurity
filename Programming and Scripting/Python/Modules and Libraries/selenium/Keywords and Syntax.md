Install selenium
```python
# go to cmd and type this command
pip install selenium
```

##### Install chrome webdriver
Visit this link: https://chromedriver.chromium.org/downloads
And download the driver based on the version of your google chrome

##### Syntax for selenium to work
```python
from selenium import webdriver  # webdriver to run the webdriver of google chrome
from selenium.webdriver.chrome.service import Service  # service is where you should input the path of the chrome webdriver you download
from selenium.webdriver.chrome.options import Options  # options to set the driver to stay open after the automation or preventing to close after nothing to automate  
from selenium.webdriver.common.by import By  # By is for finding the elements of the website by name, id, class, etc.
from selenium.webdriver.common.keys import Keys  # Keys to control the keyboard keys


options = Options()  # call the object of the options
options.add_experimental_option('detach', True)  # add options to stay open when opening the chrome driver
  
path = "C:\Program Files (x86)\chromedriver.exe"  # the path of the chrome driver where you download
service = Service(path)  # put the path variable to the service object of the selenium webdriver chrome service
driver = webdriver.Chrome(service=service, options=options)  # add all the necessary requirements of the driver including the srevice and options that are set before 
  
driver.get("https://google.com")  # call the driver and open the google website
```

##### Other function
```python
driver.title  #return the title of the website
driver.find_element(By.NAME, 'q')
	# common list other use of By
	By.ID
	By.XPATH
	By.TAG_NAME
	By.CLASS_NAME
	By.CSS_SELECTOR
	By.LINK_TEXT

# put the element on a variable to use it later
search = driver.find_element(By.NAME, 'q')
search.send_keys('what is selenium')  # enter a text on the element 
search.send_keys(Keys.ENTER)  # press the enter key on the keyboard

# in google, when you search, every clickable link is stored in h3 tag
links = driver.find_elements(By.TAG_NAME, 'h3')  
for link in links:  
    print(link.text)

```