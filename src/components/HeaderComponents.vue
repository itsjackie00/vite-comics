<template>

    <header>
        <div id="header-container">
            <div class="container d-flex justify-content-between align-items-center flex-wrap" >
                <div id="logo">
                    <img src="/img/dc-logo.png" alt="Logo">
                </div>
                <div>
                    <ul>
                        <li v-for="(item, key) in menu" :key="key">
                            <a :href="item.url">{{ item.text }}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'HeaderComponents',
    data() {
        return {
            menu: [
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

header {
    height: 130px;
    width: 100%;
    margin-top: 20px;

    #header-container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        
    }

    ul {
        display: flex;
        list-style: none;
        justify-content: center;
        align-items: center;
        height: 100%;
        font-weight: 600;


        a {
            text-decoration: none;
            color: black;
            border-bottom: 5px solid transparent;
            padding: 0px 5px 73px 0px;
            &:hover {
                color: $primary;
                border-bottom: 5px solid $primary;
                padding: 0px 5px 73px 0px;
            }
        }
        li {
            padding: 0 15px;
        }
    }
}
</style>