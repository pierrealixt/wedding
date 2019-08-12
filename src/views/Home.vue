<template>
  <div>
    <ACelebration></ACelebration>

    <MyText
      v-bind:text="{
        line1: 'Carina & Pierre-Alix'
      }"
      fontSize="16"></MyText>

    <MyWeirdText
      text='08 August 2020'></MyWeirdText>

    <MyText
      v-bind:text="{
        line1: 'Cape Town, South Africa'
      }"
      fontSize="16"></MyText>

    <MyButton
      text='RSVP'
      link='http://google.fr'></MyButton>

    <MyText
      v-bind:text="{
        line1: 'Please RSVP by January 2020',
        line2: 'More details to follow.'
      }"
      fontSize="12"></MyText>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import ACelebration from '@/components/ACelebration.vue';
import MyText from '@/components/Text.vue';
import MyWeirdText from '@/components/MyWeirdText.vue';
import MyButton from '@/components/MyButton.vue';

@Component({
  components: {
    ACelebration,
    MyText,
    MyWeirdText,
    MyButton,
  },
})
export default class Home extends Vue {}
</script>

<style lang="scss">
html {
  background: url('../assets/HeaderImage.jpg') no-repeat center center fixed;
  background-size: cover;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
}

body {
  padding-top: 3em;
}
</style>