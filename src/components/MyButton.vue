<template>
    <div>
        <a :href='link' target="_blank">{{ text }}</a>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class MyButtom extends Vue {
    @Prop() private text!: string;
    @Prop() private link!: string;
}
</script>

<style scoped>
div {
    margin: 2em;
}
a {
    background: #505B29;
    box-shadow: 0 2px 4px 0 rgba(0,0,0,0.50);
    border-radius: 12px;
    font-family: Helvetica-Bold;
    font-size: 14px;
    color: #F5F4F2;
    letter-spacing: 3.15px;
    text-align: center;
    line-height: 23px;
    padding: 10px;
    text-decoration: none;
}

a:hover {
    background: blue;
}
</style>