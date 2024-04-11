<template>
    <div id="jumbohero">
        <div class="container">
            <button type="button" class="btn fs-5">
                CURRENT SERIES</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Jumbotron',
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

#jumbohero {
    background-image: url('/img/jumbotron.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    height: 450px;
    position: relative;

    button {
        background-color: $primary;
        color: white;
        text-decoration: none;
        font-weight: 600;
        padding: 10px 20px;
        border-radius: 0;
        position: absolute;
        bottom: -20px;
        border: 3px solid $primary;

        &:hover {
            background-color: white;
            color: $primary;
            border: 3px solid $primary;
            transform: scale(1.1);
            transition: 0.5s;
        }

    }
}
</style>