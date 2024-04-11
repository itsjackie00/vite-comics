<template>
    <main>
        <div class="container py-5">
            <h3> -> Content goes here <- </h3>
             
        </div>
    </main>
</template>

<script>
    export default {
        name: 'MainComponent',
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

main{
    background-color: $background-dark;

    h3{
        color: white;
    }
}
</style>