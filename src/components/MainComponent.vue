<template>
    <main>
        <div class="my-container p-2 ">
            <div class="row">
                <div class="col-12 col-md-6 col-lg-3 mb-4" v-for="(item,index) in comics" :key="index">
                    <CardComponent :thumb="item.thumb" :price="item.price" :series="item.series" />
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