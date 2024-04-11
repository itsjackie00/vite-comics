<template>
    <footer id="footer-top">
        <div >
            <div class="row" >
                <div class="col-2 text-center align-content-center py-4" v-for="(item, key) in merchants" :key="key.id">
                    <img :src="item.img" :alt="item.text">
                    {{ item.text }}
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'FooterComponentTop',
    data(){
        return{
            merchants: [
                {   id: 1,
                    img: '/img/buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS',
                },
                {
                    id: 2,
                    img: '/img/buy-comics-merchandise.png',
                    text: 'DC MERCHANDISE',
                },
                {
                    id: 3,
                    img: '/img/buy-comics-subscriptions.png',
                    text: 'SUBSCRIPTIONS',
                },
                { 
                    id: 4,
                    img: '/img/buy-comics-shop-locator.png',
                    text: 'COMIC SHOP LOCATOR',
                },
                {   
                    id: 5,
                    img: '/img/buy-dc-power-visa.svg',
                    text: 'DC POWER VISA',
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

#footer-top{
    background-color: $primary;
    height: 150px;
    color: white;

    .container{
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;
    }

    img{
        width: 45px;
        margin-right: 10px;

        &:hover{
            cursor: pointer;
        }
    }
    
}
</style>