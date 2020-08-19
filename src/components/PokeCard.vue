<template>
   <div class="q-pa-md row items-start q-gutter-md">
    <q-card class="pokecard" flat bordered>
      <q-carousel
      animated
      v-model="slide"
      arrows
      navigation
      infinite
      autoplay
      :height="maxWidth"
      control-color="red"
    >
      <q-carousel-slide :name="1" img-src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/1.png" />
      <q-carousel-slide :name="2" img-src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/back/1.png" />
    </q-carousel>

      <q-card-section>
        <div class="text-h5 q-mt-sm q-mb-xs">bulbasaur</div>
        <div class="row">
          <div class="col"><b>Weight:</b> 320</div>
          <div class="col"><b>Height:</b> 11</div>
        </div>
        <div class="row">
         <div class="col"><b>Type:</b> grass, poison</div>
        </div>
      </q-card-section>

      <q-card-actions>
        <q-btn flat color="dark" label="Share" class="firstBtnCard"/>
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
  name: 'PokeCard',

  data() {
    return {
      maxWidth: '250px',
      slide: 1,
      expanded: false,
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
    };
  },
};
</script>

<style lang="sass" scoped>
.pokecard
  min-width: 250px
  width: 100%
  max-width: 250px
  border-radius: 2vw

.firstBtnCard
  padding-left: 1vw
  padding-right: 1vw
</style>
