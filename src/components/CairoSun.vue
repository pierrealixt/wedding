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

@media (min-width: 320px) and (max-width: 414px) {
    div {
        top: 2em;
    }
}

@media (min-width: 568px) and (max-width: 812px) {
    div {
        top: 1em;
    }
    img {
        width: 100px;
        height: 100px;
    }
}
</style>