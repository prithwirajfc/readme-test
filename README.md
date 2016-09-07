## Introduction

FusionCharts Suite XT is a front-end, JavaScript-based, comprehensive collection of 90+ charts and  1000+ maps. This includes simple and complex charts like the column and bar charts, pie and doughnut charts, treemap, heatmap, logarithmic charts, and so on; gauges like the angular gauge, bulb gauge, thermometer gauge, and so on; and maps for all continents, major countries, and all US states.

The **fusionmaps** package includes the complete FusionCharts Suite XT; along with all the charts and widgets, it includes map definition files for all maps offered by FusionCharts. 
It is recommended that you download the **fusioncharts** package if you will be needing only the charts and widgets; with just two map definition files (for the USA and world maps) the package size is smaller and can be installed faster.

* Official website: [http://www.fusioncharts.com/](http://www.fusioncharts.com/)
* Download page: [http://www.fusioncharts.com/download/](http://www.fusioncharts.com/download/)
* Licensing: [http://www.fusioncharts.com/buy/](http://www.fusioncharts.com/buy/)
* Documentation: [http://www.fusioncharts.com/dev/](http://www.fusioncharts.com/dev/)
* Support: [http://www.fusioncharts.com/support/](http://www.fusioncharts.com/support/)

## Quick Start

### Installing FusionMaps from NPM

1. Install the FusionMaps package.
   `$npm install fusionmaps`
2. Load FusionCharts using require.
   `var FusionCharts = require(‘fusioncharts’);`
3. Load the maps module using require.
   `require(‘fusioncharts/fusioncharts.maps’)(FusionCharts);`
4. Load the map definition file(s) for the map(s) to be rendered using the format:`fusioncharts.<MAP_ALIAS>.js, where MAP_ALIAS gets replaced by the map’s JavaScript alias. Click [here](http://www.fusioncharts.com/dev/getting-started/list-of-maps.html) to get the alias names for all map definition files. Map definition files for all maps to be rendered in the application have to be included.
   Assuming that you need to render the world map:
   `require(‘fusioncharts/maps/fusioncharts.world’)(FusionCharts);`

   <p class="text-info"> Unlike the core files that are stored in the **fusioncharts** directory, all map definition files are stored in the **maps** directory and are required to be fetched from there. </p>

5. Create the FusionCharts instance required to render the map.
   ```
   var chart = new FusionCharts ({
	“type”: “World”,
	“width”: “500”,
	“height”: “300”,
	“dataFormat”: “json”,
	“dataSource”: {
		chart:{}
	}
}).render(‘chartContainer’);
```

#### Adding Files for Specific Chart Types

For certain chart types, you may need to include/exclude certain files and in a certain order. These chart types and the corresponding files are mentioned below:
To render the zoom-scatter chart, it is necessary to include the **fusioncharts.js** and **fusioncharts.charts.js** files before the **fusioncharts.zoomscatter.js** file.
`var FusionCharts = require(“fusioncharts”);`
`require('fusioncharts/fusioncharts.charts')(FusionCharts);`
`require('fusioncharts/fusioncharts.zoomscatter')(FusionCharts);`

To render the treemap chart, it is necessary to include the **fusioncharts.js** and **fusioncharts.powercharts.js** files before the **fusioncharts.treemap.js** file.
`var FusionCharts = require(“fusioncharts”);`
`require('fusioncharts/fusioncharts.powercharts')(FusionCharts);`
`require('fusioncharts/fusioncharts.treemap')(FusionCharts);`

To render the SS Grid chart only the **fusioncharts.js** and the **fusioncharts.ssgrid.js** files are needed.
`var FusionCharts = require(“fusioncharts”);`
`require('fusioncharts/fusioncharts.ssgrid')(FusionCharts);`

To render the Gantt chart only the **fusioncharts.js** and the **fusioncharts.gantt.js** files are needed.
`var FusionCharts = require(“fusioncharts”);`
`require(“fusioncharts/fusioncharts.gantt”)(FusionCharts);`

### Installing FusionMaps from Bower

1. Install the FusionMaps package.
   `$bower install fusionmaps`
2. Load FusionCharts.
   `<script src=”bower_components/fusionmaps/fusioncharts.js”></script>`
3. Load the maps module.
   `<script src=”bower_components/fusionmaps/fusioncharts.maps.js”></script>`
4. Load the map definition file(s) for the map(s) to be rendered using the format:`fusioncharts.<MAP_ALIAS>.js, where MAP_ALIAS gets replaced by the map’s JavaScript alias. Click [here](http://www.fusioncharts.com/dev/getting-started/list-of-maps.html) to get the alias names for all map definition files. Map definition files for all maps to be rendered in the application have to be included.
`<script src=”bower_components/fusionmaps/maps/fusioncharts.world.js”></script>`

   <p class="text-info"> Unlike the core files that are stored in the **fusioncharts** directory, all map definition files are stored in the **maps** directory and are required to be fetched from there. </p>

5. Create the FusionCharts instance required to render the map.
   ```
   <script>
	new FusionCharts({
		“type”: “world”,
		“width”: “500”,
		“height”: “300”,
		“dataFormat”: “json”,
		“dataSource”: {
			chart:{}
		}
	}).render(‘chartContainer’);
</script>
```

#### Adding Files for Specific Chart Types

For certain chart types, you may need to include/exclude certain files and in a certain order. These chart types and the corresponding files are mentioned below:
To render the zoom-scatter chart, it is necessary to include the **fusioncharts.js** and **fusioncharts.charts.js** files before the **fusioncharts.zoomscatter.js** file.
`<script src = ”bower_components/fusioncharts/fusioncharts.js”> </script>`
`<script src = “bower_components/fusioncharts/fusioncharts.charts.js”> </script>`
`<script src = “bower_components/fusioncharts/fusioncharts.zoomscatter.js”> </script>`

To render the treemap chart, it is necessary to include the **fusioncharts.js** and **fusioncharts.powercharts.js** files before the **fusioncharts.treemap.js** file.
`<script src = ”bower_components/fusioncharts/fusioncharts.js”> </script>`
`<script src = “bower_components/fusioncharts/fusioncharts.powercharts.js”> </script>`
`<script src = “bower_components/fusioncharts/fusioncharts.treemap.js”> </script>`

To render the SS Grid chart only the **fusioncharts.js** and the **fusioncharts.ssgrid.js** files are needed.
`<script src = ”bower_components/fusioncharts/fusioncharts.js”> </script>`
`<script src = “bower_components/fusioncharts/fusioncharts.ssgrid.js”> </script>`

To render the Gantt chart only the **fusioncharts.js** and the **fusioncharts.gantt.js** files are needed.
`<script src = ”bower_components/fusioncharts/fusioncharts.js”> </script>`
`<script src = “bower_components/fusioncharts/fusioncharts.gantt.js”> </script>`

## What's Included

### Directory Structure: FusionMaps Installed via NPM
When FusionMaps is installed via NPM, the package contains the following directories and files:

node_modules/
|__ fusionmaps/
	|
	|__ package.json
	|
	|__ maps/
	|	|__ fusioncharts.world.js
	|	|__ fusioncharts.usa.js
	|	|__ fusioncharts.<MAP_ALIAS>.js
	|
	|__ themes/
	|	|__ fusioncharts.theme.carbon.js
	|	|__ fusioncharts.theme.fint.js
	|	|__ fusioncharts.theme.ocean.js
	|	|__ fusioncharts.theme.zune.js
	|
	|__ fusioncharts.js
	|__ fusioncharts.charts.js
	|__ fusioncharts.zoomscatter.js
	|__ fusioncharts.ssgrid.js
	|__ fusioncharts.powercharts.js
	|__ fusioncharts.gantt.js
	|__ fusioncharts.treemap.js
	|__ fusioncharts.widgets.js
	|__ fusioncharts.maps.js

### Directory Structure: FusionMaps Installed via Bower
When FusionCharts is installed via Bower, the package contains the following directories and files:

bower_components/
|__ fusionmaps/
	|
	|__ package.json
	|
	|__ maps/
	|	|__ fusioncharts.world.js
	|	|__ fusioncharts.usa.js
	|	|__ fusioncharts.<MAP_ALIAS>.js
	|
	|__ themes/
	|	|__ fusioncharts.theme.carbon.js
	|	|__ fusioncharts.theme.fint.js
	|	|__ fusioncharts.theme.ocean.js
	|	|__ fusioncharts.theme.zune.js
	|
	|__ fusioncharts.js
	|__ fusioncharts.charts.js
	|__ fusioncharts.ssgrid.js
	|__ fusioncharts.zoomscatter.js
	|__ fusioncharts.powercharts.js
	|__ fusioncharts.gantt.js
	|__ fusioncharts.treemap.js
	|__ fusioncharts.widgets.js
	|__ fusioncharts.maps.js
