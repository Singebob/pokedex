<template>
   <div class="q-pa-md row justify-center q-gutter-md">
     <CardPokemon />
     <CardPokemon />
     <CardPokemon />
  </div>
</template>

<script>
import CardPokemon from '@/components/cardPokemon.vue';

export default {
  name: 'app',
  components: {
    CardPokemon,
  },

};
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 350px
</style>
