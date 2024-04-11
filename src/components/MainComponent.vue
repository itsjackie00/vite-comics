<template>
    <main>
        <div class="container">
            <div class="row pt-5 pb-5  ">
                <div class="my-cards col-xl-2 col-md-3 " v-for="(item,index) in comics" :key="index">
                    <CardComponent :image="item.thumb" :title="item.series" />
                </div>
            </div>

        </div>
    </main>
</template>

<script>
import { comics } from './data/store';
import CardComponent from './CardComponent.vue';


export default {
    name: 'MainComponent',
    components: {
        CardComponent
    },
    data() {
        return {
            comics: comics
        }
    },
    mounted() {
        console.log(this.comics)
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

main {
    background-color: $background-dark;

    h3 {
        color: white;
    }
}
</style>