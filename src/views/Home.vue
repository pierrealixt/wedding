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
        css='august2020'></MyWeirdText>

      <MyText
        v-bind:text="{
          line1: 'Cape Town, South Africa'
        }"
        css='capetown'></MyText>


      <MyText
        v-bind:text="{
          line1: 'Please RSVP by January 2020',
          line2: 'More details to follow.'
        }"
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
    font-weight: bold;
  }

  .pleasersvp {
    margin-top: 3vh;
    font-size: .9em;
    line-height: 1em;
  }

  .buttonrsvp {
    margin-top: 4vh;
  }

/*
  ##Device = Desktops
  ##Screen = 1281px to higher resolution desktops
*/

@media (min-width: 1281px) {

  //CSS

}

/*
  ##Device = Laptops, Desktops
  ##Screen = B/w 1025px to 1280px
*/

@media (min-width: 1025px) and (max-width: 1280px) {

  //CSS

}

/*
  ##Device = Tablets, Ipads (portrait)
  ##Screen = B/w 768px to 1024px
*/

@media (min-width: 768px) and (max-width: 1024px) {

  //CSS

}

/*
  ##Device = Tablets, Ipads (landscape)
  ##Screen = B/w 768px to 1024px
*/

@media (min-width: 768px) and (max-width: 1024px) and (orientation: landscape) {

  //CSS

}

/*
  ##Device = Low Resolution Tablets, Mobiles (Landscape)
  ##Screen = B/w 481px to 767px
*/

@media (min-width: 481px) and (max-width: 767px) {

  //CSS
  .unefete {
    margin-top: 6vh;
    font-weight: bold;
  }

  .august2020 {
    margin-top: 6vh;
    p {
      font-size: 2.5em;
    }
  }
  .capetown {
    margin-top: 5vh;
    font-size: .7em;
  }

  .pleasersvp {
    margin-top: 2vh;
    line-height: 1.2em;
    font-size: .6em;
  }

  .buttonrsvp {
    margin-top: 6vh;
  }

}

/*
  ##Device = Most of the Smartphones Mobiles (Portrait)
  ##Screen = B/w 320px to 479px
*/

@media (min-width: 320px) and (max-width: 480px) {

  //CSS
  .unefete {
    margin-top: 5vh;
    font-weight: bold;
  }

  .carinapierrealix {
    margin-top: 6vh;
  }

  .august2020 {
    margin-top: 2vh;
    p {
      font-size: 2.5em;
    }
  }

  .capetown {
    margin-top: 3vh;
    font-size: .7em;
  }

  .pleasersvp {
    margin-top: 3vh;
    line-height: 2em;
    font-size: .6em;
  }

  .buttonrsvp {
    margin-top: 8vh;
  }
}
</style>