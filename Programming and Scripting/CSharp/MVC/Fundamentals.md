
### Controller
- act as an endpoint
- if you have "AdminController.cs", you will visit the website like this: domain:port/Admin

AdminController.cs have functions:
	public string Index()...
	public ActionResult Welcome(string firstname, string lastname)

visiting the Admin will route to Index() which is the default, to go to Welcome, go to domain:port/Admin/Welcome?firstname=Mark&lastname=Vince.
	the string is nullable, meaning you can visit the path /Admin/Welcome without parameters, if you want int and other data types to be null, you can put in the parameters (string firstname..., int? age)





















