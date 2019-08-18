<template>
    <div :class="getClass()">
        <img  src='../assets/protea.svg' alt='protea' />
    </div>
</template>
<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Protea extends Vue {
    @Prop() private position!: string;

    public getClass(): string  {
        return 'protea protea-' + this.position;
    }
}
</script>

<style scoped lang="scss">


// @media (min-width: 1025px) and (max-width: 1280px) {
//     div.protea {
//         width: 15vw;
//     }

// }

div.protea {
    position: absolute;
    bottom: 0;
    img {
        width: 192px;
        height: 300px;
    }
}

div.protea-left {
    left: 0;
}

div.protea-right {
    right: 0;
    img {
        transform: scaleX(-1);
    }
}

@media (min-width: 320px) and (max-width: 414px) {
    div.protea {
        img {
            width: 60px;
            height: 120px;
        }
    }
}

@media (min-width: 568px) and (max-width: 812px) {
    div.protea {
        img {
            width: 50px;
            height: 100px;
        }
    }
}
</style>