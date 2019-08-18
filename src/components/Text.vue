<template>
    <div :class="getCSSClasses()">
        <p v-bind:style="{fontSize: fontSize + 'px' }">
            {{ text.line1 }}
            <br />
            {{ text.line2 }}
        </p>
    </div>

</template>
<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class MyText extends Vue {
    @Prop() private text!: string;
    @Prop() private fontSize!: string;
    @Prop() private css!: string;
    public getCSSClasses(): string  {
        return this.css;
    }

}
</script>

<style scoped lang="scss">
p {
    font-family: Helvetica Neue,Helvetica,Arial,sans-serif;
    color: #FFFFFF;
    text-align: center;
    text-transform: uppercase;
    letter-spacing: 2.6px;
    margin: 0;
}
</style>