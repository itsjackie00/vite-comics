<template>
    <footer id="footer-top" class="my-container">
        <div >
            <div class="row w-100" >
                <div class="list-item  col-xl-2 col-md-5 col-sm-6   text-center align-content-center py-4  " v-for="(item, key) in merchants" :key="key.id">
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
    color: white;
    position: relative;

    .list-item{
        margin: 0 auto;
    }

    .my-container{
        width: 45%;
        margin: 0 auto;

    }

    img{
        width: 50px;
        margin-right: 10px;

        &:hover{
            cursor: pointer;
        }
    }
    
}

/* ==== MEDIA QUERY ==== */
@media screen and (min-width: 1200px) {
    #footer-top{
        .my-container{
            width: 95%;
        }
    }
}
</style>