<template>
    <div>
        <p>{{ text }}</p>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class MyWeirdText extends Vue {
    @Prop() private text!: string;
}
</script>

<style scoped lang="scss">
div {
    margin: 0;
}
p {
    font-family: 'Pacifico', cursive;
    font-size: 60px;
    color: #AEAC9B;
    margin: 0.2em;
}


</style>