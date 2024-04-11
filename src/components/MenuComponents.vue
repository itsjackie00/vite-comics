<template>
    <div class="col-xl-4 col-md-5 col-sm-9 py-4">
        <h5>{{ title }}</h5>
        <ul>
            <li v-for="(item, index) in items" :key="index">
                <a :href="item.url">{{ item.text }}</a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'MenuComponents',
    props: ['title', 'items']
}
</script>

<style lang="scss" scoped>
h5 {
    margin-left: 30px;
}

li {
    list-style: none;
    font-size: smaller;

    a {
        text-decoration: none;
        color: grey;
    }
}
</style>