ionic-select-search
====================

## Description

This is a customizable select box for ionic framework.
While the package name is "ionic-select-search", the module name is "$selectSearchBox".

Based on the awesome [ionic-Select-Control](https://github.com/OSAMES/ionic-Select-Control).

## Dependencies

This component uses ionic-modal and ionic-list from ionic framework components.
Clicking outside the modal won't close it.

## How to use

1. Install with bower:

`bower install ionic-select-search --save`

2. Include as a dependency of your angular module:

```javascript
angular.module('myApp', ['ionic', '$selectSearchBox'])
```

3. Include necessary files in your index.html header, for example linking directly to files where bower component was installed:

```HTML
   <link rel="stylesheet" href="lib/ionic-select-search/dist/select-search.min.css" >

   <script type="text/javascript" src="lib/ionic-select-search/dist/select-search.min.js"></script>
```

4. Use the select-search-box directive:

```HTML
  <select-search-box selected-value="selectedValue" 
          		item-name="label" 
          		item-id="id" 
          		select-title="Select something!" 
          		source="mySelectedValue" 
          		placeholder-text="nothing selected!"
          		select-changed="doSomethingWithSelectedValue(selectedValue)"
          		placeholder-text-class="myPlaceholderStyle"
          		>

</select-search-box>
```
 
### Directive parameters
| Name | Description |Remark |
| :------------- | :------------- | :------------- |
|selected-value|Variable from scope that will get populated with selected option value|Required. <br> Updated using two-way binding.|
|source|Scope object passed to SelectBox, format: list of object with two properties, one for label, one for value|Required.|
|item-name|Name of property for label, in scope object passed to SelectBox|Required.|
|item-id|Name of property for value, in scope object passed to SelectBox|Required.|
|placeholder-text|Placeholder string when no value is selected|Required.|
|select-title|Title of SelectBox|Required.|
|select-changed|JS function to execute after item selection.|Optional. <br> This function argument name should be 'selectedValue', both in your controller function declaration and in SelectBox select-changed attribute value (function call).|
|placeholder-text-class|CSS class to apply to placeholder|Optional.|
|select-box-class|CSS class to apply to whole select box control|Optional.|
|show-search|If `no`, search functionality will by omitted. Shown otherwise. Default = `yes`. |Optional.|
 
 **Example of object for source:**
 ```javascript
var obj = [
  {label: "Value1", id:"1"},
  {label: "Value2", id:"2"},
  {label: "Value3", id:"3"},
  {label: "Value4", id:"4"}
]
 ```

## Tests

In "test" root folder, there are some html test pages with different configurations, stylings. 
They don't require a web server to be opened, thus are kept basic.
Used libraries (ionic bundle, angular translate) are stored in "lib" root folder.
