# FusionCharts PHP Wrapper

### What is FusionCharts PHP wrapper?

FusionCharts Suite XT uses JavaScript to generate charts in the browser. Where using this PHP server side wrapper you can create charts in your PHP website without writing any Javascript code. 

### How does the wrapper work?
Charts are generated in the browsers with the help of JavaScript and the HTML code.
Using this PHP wrapper we can generate the required JavaScript and HTML code as a string in the server. We can put this strings in the page to generate charts.
l
### Version
1.0

### Requirements
PHP 5 or higher

### Installation
 * Include FusionCharts.php in your project.
 * Start using methods and classes available under **"FusionCharts.Charts"** namespace to generate Charts in your project.
 
### Program Descriptionl
##### Chart Class (FusionCharts)
Represent the FusionCharts class that can be initialized to create a chart.
###### **Constructor parameters:**
Following parameters can be used in the constructor in the order as they are described. Some parameters are optional. This function assumes that you've already included the FusionCharts JavaScript library in your page.

| Parameter | Type | Description |
|:-------|:----------:| :------|
| chartType | `String` | The type of chart that you intend to plot. e.g. `Column3D`, `Column2D`, `Pie2D` etc.|
|chartId | `String` | Id for the chart, using which it will be recognized in the HTML page. Each chart on the page needs to have a unique Id.|
|chartWidth | `String` | Intended width for the chart (in pixels). e.g. `400`|
|chartHeight | `String` | Intended height for the chart (in pixels). e.g. `300`|
|dataFormat | `String` | Type of the data that is given to the chart. e.g. `json`, `jsonurl`, `xml`, `xmlurl`|
|dataSource | `String` | Actual data for the chart. e.g. `{"chart":{},"data":[{"label":"Jan","value":"420000"}]}`|

##### Methods under Chart class
###### **Render**
Public method to generate html code for rendering chart. This function assumes that you've already included the FusionCharts JavaScript library in your page.

### Usage Guide
#### Step 1:
**Include the wrapper file in your PHP page as follows**
```php
    include("fusioncharts.php");
```
#### Step 2:
**Create the chart object with needed info as shown below**
```php
    $columnChart = new FusionCharts(
			"column2d", 
			"ex1" , 
			"600", 
			"400", 
			"chart-1", 
			"json", 
			'{  
			   "chart":
			   {  
				  "caption":"Harry\'s SuperMart",
				  "subCaption":"Top 5 stores in last month by revenue",
				  "numberPrefix":"$",
				  "theme":"ocean"
			   },
			   "data":
			   [  
				  {  
					 "label":"Bakersfield Central",
					 "value":"880000"
				  },
				  {  
					 "label":"Garden Groove harbour",
					 "value":"730000"
				  },
				  {  
					 "label":"Los Angeles Topanga",
					 "value":"590000"
				  },
				  {  
					 "label":"Compton-Rancho Dom",
					 "value":"520000"
				  },
				  {  
					 "label":"Daly City Serramonte",
					 "value":"330000"
				  }
			   ]
		}');
```
### License

**FUSIONCHARTS:**

Copyright (c) FusionCharts Technologies LLP  
License Information at [http://www.fusioncharts.com/license](http://www.fusioncharts.com/license)
