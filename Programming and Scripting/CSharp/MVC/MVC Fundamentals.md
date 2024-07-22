
### Controller
- act as an endpoint
- if you have "AdminController.cs", you will visit the website like this: domain:port/Admin

AdminController.cs have functions:
	public string Index()...
	public ActionResult Welcome(string firstname, string lastname)

visiting the Admin will route to Index() which is the default, to go to Welcome, go to domain:port/Admin/Welcome?firstname=Mark&lastname=Vince.
	the string is nullable, meaning you can visit the path /Admin/Welcome without parameters, if you want int and other data types to be null, you can put in the parameters (string firstname..., int? age)


# Migration
Enable-Migrations -ContextTypeName MvcMovie.Models.MovieDBContext
	- enable migration, creates a Configuration.cs file in a new "Migrations" folder.

add-migration Initial(initial)
	- create initial migration, and create a file {dateformat}_Initial.cs

update-database -Verbose(to see what SQL is using)
	- command to update the database
	
when you update the database, it will execute the {dateformat}\_Initial.cs to create database schema and load the seed method to populate data to the database.


note:
	- if you change the schema(attributes) of your model, you have to type "add-migration (initial migration name)"  and you have to update the database by typing "update-database"
	- doing the add-migration name_here and update-database will remove existing data and populate data from seed method




# Data Annotations in Controller
```csharp
[HttpPost]
[HttpPost, ActionName("value")]
	- "value" - name of the value in the value attribute in the input type from the form of HTML
	- used when different ActionResult or method name, it will track the value of ActionName



```



# Statement in Controller
```csharp
------ Delete specific movie based on its id
Movie movie = db.Movies.Find(id);
db.Movies.Remove(movie);
db.SaveChanges();
return RedirectToAction("Index");





```













# Data Annotation for Format and Validation of Model
```csharp
[StringLength(30)]
[StringLength(60, MinimumLength = 3)]

[Required]

[RegularExpression(@"^[A-Z]+[a-zA-Z]*$")]
[RegularExpression(@"^[A-Z]+[a-zA-Z]*$", ErrorMessage = "Only upper and lowercase")]

[Range(1, 100)]

[DataType(DataType.Currency)]



note:
	- decimal, int, float, datetime are inherently required and do not need the Required attribute.
	- you can combine different validation like this:
		[Required, StringLength(30), etc.]
	

partner validation:
	@Html.EditorFor
	@Html.ValidationMessageFor


DataType
	- not validation
	- only act as hint to the view (indirect validation)








```





























