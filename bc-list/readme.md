# BcList
Intended to be a quick way to display a list of data, without worrying about making the ajax requests.

## Dependencies
* [jQuery](https://code.jquery.com/jquery-1.12.4.min.js)
* [Handlebars](http://handlebarsjs.com/)

## Parameters

* ```containerClass``` - selector of the class you want to display your result (do not include the ".")
* ```source``` - json data source
* ```templatePath``` - path to the template used to display your data. *Note:* must be on the same domain as your app

## Usage
```javascript

//Initialize the List
var adoptedPets = new BcList({
    containerClass: "adoptable-pet-list", //Selector of class you want to append your results
    source: "//egov.baltimorecountymd.gov/LostAdoptPetService/GetAdoptablePets",
    templatePath: "/sebin/l/i/adoptable-pet.template.js"
});

adoptedPets.Show(type, function() {
  console.log('do something after you received the data via ajax');
});

```