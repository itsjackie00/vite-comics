<template>
    <div class="card" style="width: 18rem;">
        <img :src="thumb" class="card-img-top" :alt="series">
        <div class="card-body">
            <h5 class="card-title">{{series}}</h5>
            <p class="card-text">{{ price }}</p>
            <a href="#" class="btn btn-primary">Go somewhere</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardComponent',
    proprs:['thumb','price','series','type'],


}
</script>

<style lang="scss" scoped></style>