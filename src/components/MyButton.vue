<template>
    <div :class="getCSSClasses()">
        <a :href='link' target="_blank">{{ text }}</a>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class MyButtom extends Vue {
    @Prop() private text!: string;
    @Prop() private link!: string;
    @Prop() private css!: string;
    public getCSSClasses(): string  {
        return this.css;
    }

}
</script>

<style scoped>
a {
    background: #505B29;
    box-shadow: 0 2px 4px 0 rgba(0,0,0,0.50);
    border-radius: 4px;
    font-family: Helvetica-Bold;
    font-size: 21px;
    color: #F5F4F2;
    letter-spacing: 3.15px;
    line-height: 23px;
    padding: 10px 50px;
    text-decoration: none;
}

a:hover {
    background:rgb(234, 212, 199);
}
</style>