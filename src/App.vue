<script setup>
import Main from './components/Main.vue'
import Move from './Function/Move.vue'
</script>

<template>
  <body>
  <Move />
  <Main />
  </body>
</template>

<style scoped>
:root {
  --mc-color: #c9ac67;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

@font-face {
  font-family: 'mc-gamefont';
  src: url(@/assets/Font/H7GBK-Heavy.ttf) format('truetype'),
  url(@/assets/Font/H7GBK-Heavy.woff) format('woff');
}

.viewer {
  transition: 500ms ease;
  transition-delay: 0.3s;
  transition-duration: 500ms;
}

</style>
