# Install vue-design-system into nuxt.js

- Clone [https://github.com/viljamis/vue-design-system](https://github.com/viljamis/vue-design-system)

- change the package name in the ``` package.json ``` file

- Install dependencies with ``` yarn ``` or ``` npm install ```

- Create your design elements, patterns and templates

- Compile the production design system with ``` yarn run build:system ``` or ``` npm run build:system ```

- install your created design system into your nuxt.js project with ``` yarn add file:[path-to-your-design-system] ``` or ``` npm install --save file:[path-to-your-design-system] ```

- in your nuxt.js project, create a new file at: ``` plugins/designsystem.js ```

``` js
import Vue from 'vue'
import system from 'vue-design-system'
import 'vue-design-system/dist/system.css'

Vue.use(system)
```
- Import this plugin in the nuxt.config.js file: 

``` js
plugins: [
    { src: '~/plugins/designsystem', ssr: false }
]
```

Now you can use your design system within your nuxt project