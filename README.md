# vue-gtag

Global Site Tag plugin for Vue (gtag.js)

<p>
<a href="https://badge.fury.io/js/vue-gtag">
 <img src="https://badge.fury.io/js/vue-gtag.svg" />
<a/>

 <img src="https://img.shields.io/badge/size-1.80kB-brightgreen.svg" />
</p>

## Requirements

Vue ^2.0.0

## Install

```bash
npm install vue-gtag
```

## User guide

Coming soon...

For now this is all I got time to write :D

Start using it your Vue application
```js
import Vue from 'vue'
import VueGtag from 'vue-gtag'

const options = {
  config: {
    id: 'GA_MEASUREMENT_ID' // replace GA_MEASUREMENT_ID with your ID
  }
}

Vue.use(VueGtag, options)
```

Start automatic routing track by passing your VueRouter instance

```js
import Vue from 'vue'
import VueGtag from 'vue-gtag'
import VueRouter from 'vue-router'

const router = new VueRouter({
  routes: [{...}]
})

const options = {
  config: {
    id: 'GA_MEASUREMENT_ID' // replace GA_MEASUREMENT_ID with your ID
  }
}

Vue.use(VueGtag, options, router)

new Vue({
  router,
  render: h => h(App)
}).$mount("#app");
```

plugin default options

```js
{
  enabled: true,
  globalObjectName: "gtag",
  pageTrackerTemplate: () => null,
  pageTrackerShouldUpdate: () => true,
  pageTrackerEnabled: Router != null,
  pageTrackerScreenviewEnabled: false,
  config: {
    id: null,
    params: {
      send_page_view: true
    }
  }
}
```

## Notes
The package is ready for production, but might have limited features and documentation, compared to vue-analytics. In case you need more flexibility, right now I still suggest you to install [vue-analytics](https://github.com/MatteoGabriele/vue-analytics) as your main tracking system.

# Issues and features requests

Please drop an issue, if you find something that doesn't work, or a feature request at [https://github.com/MatteoGabriele/vue-gtag/issues](https://github.com/MatteoGabriele/vue-gtag/issues)

Follow me on twitter [@matteo\_gabriele](https://twitter.com/matteo_gabriele)
