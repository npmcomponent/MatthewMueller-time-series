*This repository is a mirror of the [component](http://component.io) module [matthewmueller/time-series](http://github.com/matthewmueller/time-series). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/matthewmueller-time-series`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# time-series

  Simple streaming time series graphs. Automatically scales the y-axis points based on the graph height.

  ![graph](http://i.cloudup.com/ieUMBoog5qL.png)

## Installation

    $ component install matthewmueller/time-series

## Example

```js
var graph = document.getElementById('graph')
var series = Series(graph).scale('60s')

var line = series.line()
line.color('#00BEFF')

setInterval(function() {
  line.add(rand())
}, 500)

var line2 = series.line()
line2.color('#CF3E2A')

setInterval(function() {
  line2.add(rand())
}, 1000)

function rand() {
  return Math.random() * 100 | 0
}
```

## API

### TimeSeries()

  Initialize `TimeSeries`

### TimeSeries.scale(s:String|Number)

  Set the scale


### TimeSeries.line(opts:Object)

  Create a new line

### TimeSeries.autoscale(autoscale:Boolean)

  Autoscale the y-axis. Defaults to `true`.

### Line.color(color:String)

  Set the color of the line

### Line.strokeWidth(w:Number|String)

  Set the width of the stroke

### Line.add(y:Mixed, time:Date)

  Add a point to the time series. The `time` value is optional and will default to `new Date`.

## License

  MIT
