<template>
  <div class="wrapper">
      <Main />
      <Footer />
  </div>
</template>

<script>
import Main from "../components/Main.vue"
import Footer from "../components/Footer.vue";

export default {
  components: { Main, Footer },
  data() {
  }
}
</script>

<style>
  ul[class],
  ol[class] {
      padding: 0;
  }
  body,
  h1,
  h2,
  h3,
  h4,
  p,
  ul[class],
  ol[class],
  li,
  figure, s
  figcaption,
  blockquote,
  dl,
  dd {
      margin: 0;
  }
  ul,
  ol,
  li {
      list-style: none;
  }
  a {
      text-decoration: none;
      color: #000;
  }
  input {
      padding: 0px;
      outline: none;
  }
  button {
      padding: 0;
      border: none;
      font: inherit;
      color: inherit;
      background-color: transparent;
      cursor: pointer;
  }
  * {
      font-family: 'Montserrat', sans-serif;
      font-weight: 400;
  }
  html {
      overflow-x: hidden;
  }
  body {
      overflow-x: hidden;
  }

  .wrapper {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
  }
</style>
