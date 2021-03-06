# v-chart-plugin

> a plugin for adding charts to Vue

## Usage

First include the plugin in your main.js:

```JavaScript
import Chart from './v-chart-plugin.js'

Vue.config.productionTip = false

Vue.use(Chart);
```

Within your component you will need to include an object in your title, selector, width, height, and datapoints to pass to the component

```JavaScript
export default {
  name: 'example',
  data () {
    return {
      chartData: {
        selector: "chart",
        title: "Important Data",
        width: 300,
        height: 200,
        data: [120, 140, 70, 90, 110, 65, 210]      }
    }
  }
}
```

Lastly you will need to add the component and bind the data to it

```
<v-chart v-bind:chartData="chartData"></v-chart>
```

If you wish to style the components of the chart you can via the selectors:

```html
<style>
  .chart-bar {
    fill:blue;
  }
</style>
```
![screenshot](https://res.cloudinary.com/practicaldev/image/fetch/s--nBmlCUJ2--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/7bu2p3740cfn3cq3qygm.png)

Currently only supports bar graph for a single metric

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
