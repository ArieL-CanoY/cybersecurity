#### Advanced Searching

```bash
site: [site name] [options] - search in a site with options

  

Options:

	cache: [cache version] - when the keywords was indexed by crawlers
	
	intitle: [keyword] - search for the keyword that has on the title like login
	
	inurl: [keyword] - search for the keyword that has on the url like login or admin
	
	intext: [keyword] - search for the keyword that has on the website
	
	"[exact keywords]" - search for exact keywords 
	
	filetype: [file types] - search files based on the filetype
```



#### Examples
```bash
	site:facebook.com intext:clementine madrugal
	site:facebook.com inurl:admin
	site:facebook.com inurl:database
```