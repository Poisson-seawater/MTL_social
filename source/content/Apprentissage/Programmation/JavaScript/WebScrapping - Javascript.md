#javascript
###### sitographie
https://www.youtube.com/watch?v=TzZ3YOUhCxo
- regarder si le site de compagnie sur lequel le WebScrapping tourne offre API ->pour éviter d'avoir IP ban. 
- Livrary: puppeteer

https://www.w3schools.com/js/default.asp

## note w3s
JavaScript accepts both double and single quotes, " " et ' '.

javaScript Can Change HTML: 
- Attribute Values, like a image
- Content, like a texte
- CSS
- hide/show HTML element
With the methods `getElementById()` -> appel un élément du HTML pour le changer.

```js
<button onclick="document.getElementById('myImage').src='pic_bulbon.gif'">Turn on the light</button>

<img id="myImage" src="pic_bulboff.gif" style="width:100px">

<button onclick="document.getElementById('myImage').src='pic_bulboff.gif'">Turn off the light</button>
```


In HTML, JavaScript code is inserted between `<script>` and `</script>` tags.
Scripts can be placed in the `<body>`, or in the `<head>` section of an HTML page, or in both.
Write as:
```js
<script>  
function myFunction() {  
  document.getElementById("demo").innerHTML = "Paragraph changed.";  
}  
</script>
```

or can call a script from an external file. External scripts are practical when the same code is used in many different web pages.
You can place an external script reference in `<head>` or `<body>` as you like.
```js
<script src="myScript.js"></script>
```


