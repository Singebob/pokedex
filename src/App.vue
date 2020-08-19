<template>
   <div class="q-pa-md row justify-center q-gutter-md">
     <PokeCard />
     <PokeCard />
     <PokeCard />
  </div>
</template>

<script>
import PokeCard from '@/components/PokeCard.vue';

export default {
  name: 'app',
  components: {
    PokeCard,
  },

};
</script>

<style lang="sass">
body
  background-image: url('./assets/pokeball.svg')
  background-repeat: no-repeat
  background-position: center
  background-size: 100%
  background-attachment: fixed

</style>
