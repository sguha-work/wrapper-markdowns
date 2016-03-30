# FusionCharts JSP Wrapper

### What is FusionCharts JSP wrapper?

The FusionCharts java server-side wrapper lets you create charts in your JSP website without writing any JavaScript code.

### How does this wrapper work?
Conventionally, FusionCharts Suite XT uses JavaScript and HTML to generate charts in the browser. The JSP wrapper lets you generate the required JavaScript and HTML code as a string on the server. This string is then used to render charts on a browser page.

### Version
1.0

### Requirements
JAVA 6 or higher

### Installation
 * Download the **[`JSP wrapper package`](http://www.fusioncharts.com/jsp-charts/)**
 * Unzip the archive and move to "/jsp-wrapper-master/src/java/fusioncharts/" to get the main class file "FusionCharts.java"
 * Include "FusionCharts.java" in your project(Check **[the usage guide](http://www.fusioncharts.com/dev/using-with-server-side-languages/java/introduction.html)** for details).
 * Start using the methods and classes available under the **FusionCharts** namespace to generate charts in your project.. 
 
**Note : FusionCharts JS libraries should already be installed within your project in order to work with this wrapper.**

### Usage Guide

#### Installing FusionCharts JS libraries in your page where you want to display FusionCharts
There are two ways you can install FusionCharts JS libray in your project
* Using FusionCharts CDN
* Using library files placed in the folder of your project

**Using FusionCharts CDN**

Write a script tag in the <head> section of the page where you want to add the source of the FusionCharts library link from the official CDN:
```html
<script type="text/javascript" src="http://static.fusioncharts.com/code/latest/fusioncharts.js"></script>
```
**Using library files placed in a folder of your project**

You can download the **[`trial version`](http://www.fusioncharts.com/download/)** of FusionCharts.

Assuming you have the FusionCharts library placed inside the folder "fusioncharts" in your project, now write a script tag in the <head> section of the page where you add the src of FusionCharts libary link from local folder
```html
<script type="text/javascript" src="fusioncharts/fusioncharts.js"></script>
```
Now, you are ready to prepare the chart using our JSP-wrapper.
#### Using the wrapper
#### Step 1:
**Include the wrapper file (`FusionCharts.java`) to your JSP page:**
```JSP
    <%@page import="FusionCharts" %>
```
#### Step 2:
**Create the chart object with needed info as shown below. For details about the constructor and it's parameters check [constructor parameters](#constructor-parameters)**
```JSP
<%
    FusionCharts area2dChart = new FusionCharts(
        "Area2D",// chartType
        "myFirstChart",// chartId
        "600","400",// chartWidth, chartHeight
        "chart",// chartContainer
        "json",// dataFormat
        "{\"chart\":{\"caption\":\"Harry\\'sSuperMart\",\"subCaption\":\"Top 5 stores in last month by revenue\",\"numberPrefix\":\"$\",\"theme\":\"ocean\"},\"data\":[{\"label\":\"Bakersfield Central\",\"value\":\"880000\"},{\"label\":\"Garden Grooveharbour\",\"value\":\"730000\"},{\"label\":\"Los Angeles Topanga\",\"value\":\"590000\"},{\"label\":\"Compton-Rancho Dom\",\"value\":\"520000\"},{\"label\":\"Daly City Serramonte\",\"value\":\"330000\"}]}"
);
%>
```

#### Step 3:
**Render the chart**
```JSP
 <%=area2dChart.render()%>
```

### **Constructor parameters:**
Following parameters can be used in a constructor in the order they are described. Some parameters are optional. This function assumes that you've already included the FusionCharts JavaScript library to your page.

| Parameter | Type | Description |
|:-------|:----------:| :------|
| chartType | `String` | The type of chart that you intend to plot. e.g. `Column3D`, `Column2D`, `Pie2D` etc.|
|chartId | `String` | Id for the chart, using which it will be recognized in the HTML page. Each chart on the page should have a unique Id.|
|chartWidth | `String` | Intended width for the chart (in pixels). e.g. `400`|
|chartHeight | `String` | Intended height for the chart (in pixels). e.g. `300`|
|dataFormat | `String` | Type of data used to render the chart. e.g. `json`, `jsonurl`, `xml`, `xmlurl`|
|dataSource | `String` | Actual data for the chart. e.g. `"{\"chart\":{},\"data\":[{\"label\":\"Jan\",\"value\":\"420000\"}]}"`|

##### Methods under Chart class
###### **Render**
Public method to generate html code for rendering chart. This function assumes that you've already included the FusionCharts JavaScript library to your page.


### License

**FUSIONCHARTS:**

Copyright (c) FusionCharts Technologies LLP  
License Information at [http://www.fusioncharts.com/license](http://www.fusioncharts.com/license)


