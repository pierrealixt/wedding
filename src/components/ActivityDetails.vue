<template>
    <div>
        <p>
            <ul>
                <li><b>Time:</b> {{ time }}</li>
                <li><b>Location:</b> {{ location }}</li>
                <li><b>Dresscode:</b> {{ dresscode }}</li>
            </ul>
        </p>
        <p>
            Notes: <span v-html="notes"></span>
        </p>
    </div>

</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class ActivityDetails extends Vue {
    @Prop() private time!: string;
    @Prop() private location!: string;
    @Prop() private dresscode!: string;
    @Prop() private notes!: string;

}
</script>

<style scoped lang="scss">
div {
    margin-top: 60px;
    padding: 40px;
    @media (min-width: 320px) and (max-width: 480px) {
        margin-top: 10px;
        padding: 10px;
    }
}
p {
    color: #181818;
    text-align: left;
    font-size: 16px;
    letter-spacing: 2.31111px;
    line-height: 20px;
    margin: 20px 0;
    text-transform: none;
}
ul {
    margin: 0;
    padding: 0;
    list-style: none;
}

li {
    margin: 20px 0;
}
</style>