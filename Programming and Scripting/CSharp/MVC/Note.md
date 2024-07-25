

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



