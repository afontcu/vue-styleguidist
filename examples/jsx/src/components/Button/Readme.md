Basic button:

```jsx
<Button>Push Me</Button>
```

Big pink button and small blue button:

```vue
<Button size="large" color="deeppink">
  Click Me
</Button>
<br />
<Button size="small" color="blue">
  Second button
</Button>
```

And you _can_ **use** `any` [Markdown](http://daringfireball.net/projects/markdown/) here.

Fenced code blocks with `vue`, `js`, `jsx` or `javascript` languages are rendered as a interactive playgrounds:

```jsx
<Button>Push Me</Button>
```

You can also use the Single File Component Format

```vue
<template>
    <div class="wrapper">
        <Button @click.native="pushButton">Push Me</Button>
        <hr />
        <p class="text-name">Next Dog Name: {{ dogName }}</p>
    </div>
</template>
<script>
const dogNames = require('dog-names').all

// You can also use 'export default {}' style module exports.
export default {
  data() {
    return { numClicks: 0, dogName: dogNames[0] }
  },
  methods: {
    pushButton() {
      this.numClicks += 1
      this.dogName = dogNames[this.numClicks]
    }
  }
}
</script>
<style scoped>
.wrapper {
  padding: 10px;
}
.text-name {
  color: red;
}
</style>
```
