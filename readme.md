# Install vue-design-system into nuxt.js

- Clone [https://github.com/viljamis/vue-design-system](https://github.com/viljamis/vue-design-system)

- change the package name in the ``` package.json ``` file

- Install dependencies with ``` npm install ```

- Change the config file: ``` /build/webpack.system.conf.js ``` (search for the variable ``` libraryTarget ``` and change the value to ``` commonjs2 ```)

- Create your design elements, patterns and templates

- Compile the production design system with ``` npm run build:system ```

- install your created design system into your nuxt.js project with ``` yarn add file:[path-to-your-design-system] ``` or ``` npm install --save file:[path-to-your-design-system] ```

- in your nuxt.js project, create a new file at: ``` plugins/designsystem.js ```

``` js
import Vue from 'vue'
import system from '[your-design-system-name]'
import '[your-design-system-name]/dist/system.css'

Vue.use(system)
```
- Import this plugin in the nuxt.config.js file: 

``` js
plugins: [
    ['~/plugins/designsystem']
]
```

Now you can use your design system within your nuxt project