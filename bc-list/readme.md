# BcList
Intended to be a quick way to display a list of data, without worrying about making the ajax requests.

## Dependencies
* [jQuery](https://code.jquery.com/jquery-1.12.4.min.js)
* [Handlebars](http://handlebarsjs.com/)

## Parameters

* ```containerClass``` - selector of the class you want to display your result (do not include the ".")
* ```source``` - json data source
* ```templatePath``` - path to the template used to display your data. *Note:* must be on the same domain as your app

## Methods
### Show
After a new list is created, use the show message, to you know, show the list

```javascript
myList.Show(ajaxData, function() {
  console.log('do something after you received the data via ajax');
});
```

## Usage

### Html
```html
<body>
<h1>My awesome page</h1>
  <div class="target-container">
    <!-->Results will be displayed here</!-->
  </div>
</body>
```
### JavaScript
```javascript

//Initialize the List
var myList = new BcList({
    containerClass: "target-container", //Selector of class you want to append your results
    source: "//egov.baltimorecountymd.gov/my-awesome-app/data",
    templatePath: "/templates/my-awesome-app.template.js"
});

myList.Show(ajaxData, function() {
  console.log('do something after you received the data via ajax');
});

```