<template>
    <div>
        <p>A celebration</p>
    </div>
</template>
<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class ACelebration extends Vue {
//   @Prop() private msg!: string;
}
</script>

<style scoped lang="scss">
div {
    margin-bottom: 7em;
}
p {
    text-transform: uppercase;
    font-family: Helvetica;
    font-size: 12px;
    color: #F5F4F2;
    letter-spacing: 2.6px;
    line-height: 23px;
}
</style>