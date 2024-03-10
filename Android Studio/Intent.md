

```java
// starting new activity class

Intent varname = new Intent(this, <class name>.class);
startActivity(varname);

// passing data to other class
Intent varname = new Intent(this, <class name>.class);
varname.putExtra(<value name>, <value>);
startActivity(varname);

// on the other class
Intent varname = getIntent();
datatype varname = get<datatpe>Extra('value name');










```
















