<template>
    <footer id="footer-top">
        cioqui
        <div class="container-fluid">
            <div class="row">
                <div class="col-3">
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'FooterComponentTop',
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

#footer-top{
    background-color: $background-dark;
}
</style>