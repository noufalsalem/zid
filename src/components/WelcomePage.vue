<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p class="desc">
      Tested on Google Chrome and Microsoft Edge, <br> running at local host 8080.
    </p>
    <h3> The Tools I Used: </h3>
    <ul> 
      <li><a href="https://vuejs.org/" target="_blank" rel="noopener">VueJS (Vue 3)</a></li>
      <li><a href="https://cli.vuejs.org/" target="_blank" rel="noopener">Vue CLI 5.0.8</a></li>
      <li><a href="https://www.typescriptlang.org/" target="_blank" rel="noopener">Typescript 4.5.5</a></li>
    </ul>
    <h3>The CLI Plugins I used: </h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-router" target="_blank" rel="noopener">router</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-typescript" target="_blank" rel="noopener">typescript</a></li>
    </ul>
    <h3>Other Toolkit/CSS Framework I used:</h3>
    <ul>
      <li><a href="https://getbootstrap.com/" target="_blank" rel="noopener">Bootstrap</a></li>
      <li><a href="https://fontawesome.com/icons" target="_blank" rel="noopener">Font Awesome Icons</a></li>
    </ul>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
    msg: String
  }
})
export default class WelcomePage extends Vue {
  msg!: string
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin: 40px 0 0;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  font-weight: bold;
  color: #86589E;
}
.desc {
  font-size:medium;
}
</style>
