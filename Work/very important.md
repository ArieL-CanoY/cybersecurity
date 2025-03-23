
```
in report builder, use parameter for connection "[@ctx]"
```

```
alter the table from test and live database
```

```
before making a function, take a look at the other code of how they did it or if there is existing function.
```

```
this scripts should be separated when importing to specific site
frontendbackendnewwindow
backendnewwindows
```


```
port 80 is live
port 8008 is staging for SAVER nakatutok sa OneIBAS_Test
port 7007 is staging for MACAire nakatutok sa OneIBAS_Test
```


```
initialization before dynamiccallback
```


![[Pasted image 20241121104150.png]]



```
make sure to include the file before committing it
```

```
if problem exist, try to see what you commit
```

```
if visiting a page gives you unable to process request, check if there are files the server cannot get, or refer to the previous note
```

```
report page mvc - to show parameter on the page that will add to the parameters on backend, it should be empty first like this:

	string searchText = String.Empty;
	
	string connectingString = ConfigurationManager.ConnectionStrings["OneIBASConnection"].ConnectionString;
	
	List<ReportParameter> parameters = new List<ReportParameter>();
	parameters.Add(new ReportParameter("searchText", searchText));
	parameters.Add(new ReportParameter("DivisionCode", CurrentUser.CurrentDivisionCode));
	parameters.Add(new ReportParameter("Ctx", connectingString));
	
	return parameters;


```

```
Every table update should make the object on a table like this:
	db.Entry(<objectToUpdate>).State = System.Data.Entity.EntityState.Modified;
	db.SaveChanges()

NOTE: OBJECT SHOULD BE A TABLE AND NOT A VIEW

```


```
in datatable, if you multiple request, put the data in a single controller function so it will request only 1 and get all the necessary data  
```

```
when using string with variable:
use this instead: 'the name is ' + name;
don't use this: `the name is ${name}`
```

```
Visual Studio cannot attach to the browser fixed:
In the visual studio, when runnning the project in debug mode and if says it cannot attach to the browser, close the browser that new tab pop up when running it. Example if you run then a tab on google chrome show up but blank url, then close the google chrome. 
```

```
always put the sql executed on a notepad so that if the database is altered or revert, then there is a backup for reverting all the newly added tables and alters, and also data
```

```
in SQL, use varchar instead of text if the data is many characters because compaing to '' does not work and text is deprecated
```

```
if downloading the report cause an error to data source, try to download the report then input username and password to the data source setting then save(make sure you are connected to the server when saving)
```

```
using the optimization code, if clicking other menu then the current screen goes to the bottom and visible, check if the className is properly named. i mean this = .hideAllForms should be in the .csthml
```

```
divisioncode

snf instead of snd
cpn(new) instead of ocn(old)

```

```
in report builder, to view the dataset used in table, click any part of the table, click the top left of the table or the box, it will show the properties on the right side of the screen, look for general category, then look for DataSetName.
```














