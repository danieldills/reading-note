## Local Storage
(https://diveinto.html5doctor.com/storage.html)
What is HTML Storage?
It is a way for web pages to store named key/value pairs locally, with the client web browser.

- There's a way to check for HTML5 Storage 

```
function supports_html5_storage() {
    try {
        return 'localStorage' in window && window['localStorage'] !== null;        
    } catch (e) {
        return false;
    }
}
```
- "HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats." (source above)

```
interface Storage {
  getter any getItem(in DOMString key);
  setter creator void setItem(in DOMString key, in any data);
};
```


HTML5 Storage Support (browsers that support)
- IE 8.0+
- Firefox 3.5+
- Safari 4.0+
- Chrome 4.0+
- Opera 10.5+
- Iphone 2.0+
- Android 2.0+

