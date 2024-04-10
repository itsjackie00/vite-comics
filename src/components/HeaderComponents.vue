<template>

    <header class="container-fluid">
        <div id="header-container">
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
        height: 100%;
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
        }

        a:hover {
            color: $primary;
        }

        li {
            padding: 0 15px;
        }
    }
}
</style>