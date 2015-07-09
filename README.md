# mg-regions

A metrics-graphics addon allowing region annotations for line charts.

![example](https://raw.githubusercontent.com/senseyeio/mg-regions/master/dev/images/example.jpg "mg-regions example")

### Usage

Install using bower:

- `bower install senseyeio/mg-regions --save`

Include `dist/mg_regions.js` in your build, or include it in your HTML:

- `<script src="bower_components/mg_regions/dist/mg_regions.js"></script>`

Import the default styles from `dist/mg_regions.css`, or create your own:

- `<link rel="stylesheet" href="bower_components/mg_regions/dist/mg_regions.css" type="text/css" />`

Add regions to your line charts by specifing a regions argument in the chart options. This argument should contain an array of regions, each made up of an array specifing the start and end points and a label. For example, the following produces a region between 1994 and 2004 with a label 'friends':

```js
regions: [{
  date: [1994, 2004],
  label: 'friends', //optional
  class: 'css-class-to-apply' //optional
}]
```

### Other Options

The following optional options should be set against the root of the options object:

 - `regions_overlap_fn` : if set, will replace the default function which handles horizontal overlap. The specified function should expect two arguments, the first being the region labels, the second being the options object

### Development

- `npm start` to run a development version of the library to experiment with

### Testing

- `gulp test` to run the Test'em server in continuous mode.
- `npm test` for a single run, CI mode.