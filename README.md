# DOM-Based-XSS
HTML COM written site that is vulnerable to XSS

## Why is the site vulnerable
```
var uri_dec = decodeURIComponent(document.location.href.substring(document.location.href.indexOf("test")))
```
- ```document.location.href.indexOf("test")``` returns the index of the string inside the current page's url
- ``` document.location.href.substring(...) ``` returns the substring of the url based on the idex of the found string

```
document.write(uri_dec)
```
- The write() method writes HTML expressions or JavaScript code to a document

Special thanks to W3 schools for giving me a quick reference on the HTML DOM objects

### Reference:   
The Location Object    
https://www.w3schools.com/jsref/obj_location.asp

Location href Property    
https://www.w3schools.com/jsref/prop_loc_href.asp
