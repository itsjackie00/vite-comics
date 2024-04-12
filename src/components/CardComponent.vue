<template>
    <div class="my-card mt-5 ">
        <img :src="image" class="card-img-top" :alt="title">
        <div>
            <h5 id="card-title" class="text-white m-4 text-center">{{ title }}</h5>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardComponent',
    props: ['image', 'title', 'text', 'link'],


}
</script>

<style lang="scss" scoped>
img {
    height: 15rem;
    height: 15rem;

    &:hover {
        transform: scale(1.1);
        transition: 0.5s;
        cursor: pointer;
        opacity: 0.5;
        transition: 0.5s;
    }
}
</style>