<template>
    <main>
        <div class="container">
            <div class="row pt-5 pb-5  ">
                <div class="my-cards col-xl-2 col-md-3 " v-for="(item,index) in comics" :key="index" >
                    <CardComponent :image="item.thumb" :title="item.series"  />

                    <span id="comic-price" class="text-white hide text-center " >
                        {{ item.type }}  {{ item.price }}
                    </span>
                    <div class="hide" id="button">
                        <button class="btn btn-primary w-100 text-white">
                        <a :href="item.url">BUY NOW</a>
                    </button>
                    </div>
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
            comics: comics,
            showOnHover: false
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

    #comic-price {
       display: none;
   } 
   
    h3 {
        color: white;
    }
    /* .hide{
        display: none;
    } */

    .my-cards {
        margin-bottom: 30px;
    }

    .my-cards:hover #comic-price,
    .my-cards:hover #button {
        display: block;

    }
}
</style>