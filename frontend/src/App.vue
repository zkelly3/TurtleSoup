<template>
  <TurtleSoup/>
</template>

<script>
import TurtleSoup from './components/TurtleSoup.vue'

export default {
  name: 'App',
  components: {
    TurtleSoup
  }
}
</script>

<style lang="scss">
@use './styles/colors.scss';

/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: colors.color(grey-200);
}
 
/* Handle */
::-webkit-scrollbar-thumb {
  background: colors.color(grey-600); 
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: colors.color(grey-700); 
}


</style>
