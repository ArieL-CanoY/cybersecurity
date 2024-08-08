

when putting the value of a property of a model like this (on @Model.Stock):
```html
<input type="number" class="form-control" id="productStock" value="@Model.Stock" />
```

it should be no space, because it will cause an error if the value of the model is number but the value of value attribute has space on it.
in short, you should not be doing like this:
```html
<input type="number" class="form-control" id="productStock" value="  @Model.Stock " />
```
but this:
```html
<input type="number" class="form-control" id="productStock" value="  @Model.Stock " />
```



---
find specific id from specific tag
structure:
	form: id=form1
		h1: id=h1
	form: id=form2
		h1: id=h1
		

to find h1 id from form2 id, we need to reference the form2 id

(search this on jquery)
```javascript
var Form2h1 = $("#form2").Find("h1");

```

