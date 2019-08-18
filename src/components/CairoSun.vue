<template>
    <div class='cairo-sun'>
        <img src='../assets/cairosun_25.png' alt='Cairo Sun' />
    </div>
</template>
<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class CairoSun extends Vue {

}
</script>

<style scoped lang="scss">
@media (min-width: 320px) and (max-width: 414px) {
    img {
        width: 100px;
        height: 100px;
    }
}

@media (min-width: 1025px) and (max-width: 1280px) {
    img {
        width: 255px;
        height: 256px;
    }
}

@keyframes float {
    0% {
        transform: translatey(0px);
    }
    50% {
        transform: translatey(-20px);
    }
    100% {
        transform: translatey(0px);
    }
}
div {
    position: absolute;
    top: 0;
    right: 0;
    img {
        animation: float 6s ease-in-out infinite;
    }
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
  div {
    img {
        width: 120px;
        height: 120px;
    }
  }

}

/*
  ##Device = Most of the Smartphones Mobiles (Portrait)
  ##Screen = B/w 320px to 479px
*/

@media (min-width: 320px) and (max-width: 480px) {

  //CSS

}
</style>