<template>
    <main>
        <div class="container">
            <div class="row pt-5 pb-5  ">
                <div class="my-cards col-xl-2 col-md-3 " v-for="(item, index) in comics" :key="index">
                    <CardComponent :image="item.thumb" :title="item.series" />
                    <span id="comic-price" class="text-white hide text-center ">
                        {{ item.type }} {{ item.price }}
                    </span>
                    <div class="d-flex justify-content-between mt-2 " >
                        <button id="button" class="btn hide btn-primary text-white" @click="purchaseItem(item)">
                            <a :href="item.url">BUY NOW</a>
                        </button>
                        <button id="remove-btn" @click="removeItem(item)" class="btn btn-danger hide"> X </button>
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
        }

    },
    methods: {
        purchaseItem(item) {
            item.clickCount++;
            console.log(item.clickCount);
            if (item.clickCount %2 === 0) {
                this.comics.push(item);

            } 
        },
        removeItem(item){
            const index = this.comics.indexOf(item);
            if (index !== -1) {
                this.comics.splice(index, 1);
            }
        }
    },

    mounted() {
        this.comics = this.comics.map(comic => ({ ...comic, clickCount: 0 }));
        console.log(this.comics);
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

    .hide{
        display: none;
    }
    .count {
        position: relative;
        background-color: white;
        color: $primary;
    }
    .my-cards {
        margin-bottom: 30px;
    }

    .my-cards:hover #comic-price,
    .my-cards:hover #button,
    .my-cards:hover #remove-btn {
        display: block;

    }

    
}
</style>