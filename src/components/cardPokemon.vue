<template>
   <div class="q-pa-md row items-start q-gutter-md">
    <q-card class="my-card" flat bordered>
      <q-img
        src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/1.png"
      />

      <q-card-section>
        <div class="text-h5 q-mt-sm q-mb-xs">bulbasaur</div>
        <div class="row">
          <div class="col">Poids: 320</div>
          <div class="col">Taille: 11</div>
        </div>
      </q-card-section>

      <q-card-actions>
        <q-btn flat color="dark" label="Share" />
        <q-btn flat color="primary" label="Book" />

        <q-space />

        <q-btn
          color="grey"
          round
          flat
          dense
          :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
          @click="expanded = !expanded"
        />
      </q-card-actions>

      <q-slide-transition>
        <div v-show="expanded">
          <q-separator />
          <q-card-section class="text-subitle2">
            {{ lorem }}
          </q-card-section>
        </div>
      </q-slide-transition>
    </q-card>
  </div>
</template>

<script>

export default {
  name: 'CardPokemon',

  data() {
    return {
      expanded: false,
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
    };
  },
};
</script>

<style lang="sass" scoped>
.my-card
  min-width: 250px
  width: 100%
  max-width: 350px
</style>
