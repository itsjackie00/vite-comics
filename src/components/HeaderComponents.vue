<template>

    <header>
        <div id="header-container">
           <ul class="debug">
              <img src="/img/dc-logo.png" alt="Logo">
                <li v-for="(item, key) in menu" :key="key">
                   <a :href="item.url">{{ item.text }}</a>
                </li>
            </ul>
        </div>
    </header> 
</template>

<script>
export default {
    name: 'HeaderComponents',
    data() {
        return {
            menu:[
                {
                    text: 'CHARACTERS',
                    url: '#'
                },
                {
                    text: 'COMICS',
                    url: '#'
                },
                {
                    text: 'MOVIES',
                    url: '#'
                },
                {
                    text: 'TV',
                    url: '#'
                },
                {
                    text: 'GAMES',
                    url: '#'
                },
                {
                    text: 'COLLECTIBLES',
                    url: '#'
                },
                {
                    text: 'VIDEOS',
                    url: '#'
                },
                {
                    text: 'FANS',
                    url: '#'
                },
                {
                    text: 'NEWS',
                    url: '#'
                },
                {
                    text: 'SHOP',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
.debug{
    border: 1px solid red;
}
ul{
    display: flex;
    list-style: none;
    justify-content: center;

    li{
        padding: 0 15px;
    }
}
</style>