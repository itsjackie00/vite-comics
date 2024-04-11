<template>
    <main>
        <div class="container">
            <div class="row pt-5 pb-5  ">
                <div class="my-cards col-xl-2 col-md-3 " v-for="(item,index) in comics" :key="index" >
                    <CardComponent :image="item.thumb" :title="item.series"  />

                    <span id="comic-price" class="text-white hide text-center " >
                        {{ item.type }}  {{ item.price }}
                    </span>
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

    .my-cards {
        margin-bottom: 30px;
    }

    .my-cards:hover {
        cursor: pointer;
        opacity: 0.5;
        transition: 0.5s;

    }

    .my-cards:hover #comic-price{
        display: block;

    }
}
</style>