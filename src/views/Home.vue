<template>
  <div>
    <CairoSun></CairoSun>

    <Protea
      position='left'></Protea>

    <Protea
      position='right'></Protea>

    <div class='container'>
      <MyText
        v-bind:text="{
          line1: 'une fête'
        }"
        css='unefete'></MyText>


      <MyText
        v-bind:text="{
          line1: 'Carina & Pierre-Alix'
        }"
        fontSize="16"
        css='carinapierrealix'></MyText>

      <MyWeirdText
        text='08 August 2020'
        css='8august2020'></MyWeirdText>

      <MyText
        v-bind:text="{
          line1: 'Cape Town, South Africa'
        }"
        fontSize="16"
        css='capetown'></MyText>


      <MyText
        v-bind:text="{
          line1: 'Please RSVP by January 2020',
          line2: 'More details to follow.'
        }"
        fontSize="12"
        css='pleasersvp'></MyText>
      <MyButton
        text='RSVP'
        link='https://forms.gle/4F6nzCknEHzq7xLA7'
        css='buttonrsvp'></MyButton>
    </div>

  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import ACelebration from '@/components/ACelebration.vue';
import MyText from '@/components/Text.vue';
import MyWeirdText from '@/components/MyWeirdText.vue';
import MyButton from '@/components/MyButton.vue';
import CairoSun from '@/components/CairoSun.vue';
import Protea from '@/components/Protea.vue';

@Component({
  components: {
    ACelebration,
    MyText,
    MyWeirdText,
    MyButton,
    CairoSun,
    Protea,
  },
})
export default class Home extends Vue {}
</script>

<style lang="scss">
// @media (min-width: 320px) and (max-width: 1024px) {
//   // 480px
//   html {
//     background: url('../assets/wedding_mobile.jpg') no-repeat center right fixed;
//     background-size: cover;
//     -webkit-background-size: cover;
//     -moz-background-size: cover;
//     -o-background-size: cover;
//   }
// }

// @media (min-width: 1025px) and (max-width: 1280px) {

  html {
    background: url('../assets/wedding_desktop.jpg') no-repeat center center fixed;
    background-size: cover;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
  }

  .unefete {
    margin-top: 20vh;
    font-weight: bold;
  }

  .carinapierrealix {
    margin-top: 2vh;
  }

  .capetown {
    margin-top: 3vh;
  }

  .pleasersvp {
    margin-top: 3vh;
    line-height: 2em;
  }

  .buttonrsvp {
    margin-top: 4vh;
  }

    @media (min-width: 568px) and (max-width: 812px) {
    .unefete {
      margin-top: 3vh;
      font-weight: bold;
    }

    .capetown {
      margin-top: 1vh;
    }

    .pleasersvp {
      margin-top: 2vh;
      line-height: 1em;
    }

    .buttonrsvp {
      margin-top: 6vh;
    }


  }

</style>