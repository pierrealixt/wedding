<template>
    <div :class="getCSSClasses()">
        <p>{{ text }}</p>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class MyWeirdText extends Vue {
    @Prop() private text!: string;
    @Prop() private css!: string;
    public getCSSClasses(): string  {
        return this.css;
    }
}
</script>

<style scoped lang="scss">
p {
    font-family: Pacifico-Regular;
    font-size: 5rem;
    color: #FFFFFF;
    margin: 0;
    padding: 0;
    // letter-spacing: 6.58px;
    // line-height: 37px;
}

@media (min-width: 320px) and (max-width: 414px) {
   p {
    font-size: 3rem;
   }
}


</style>