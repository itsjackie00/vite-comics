<template>
    <footer id="footer-bottom">
        <div class="my-container">
            <button type="button" class="btn btn-link">SIGN-UP NOW!</button>
        </div>
       
    </footer>
</template>

<script>
    export default {
        name: 'FooterComponentBottom',
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

#footer-bottom{
    background-color: #303030;
    height: 130px;
    position: relative;

    .my-container{
        width: 87%;
        margin: 0 auto;
    }

    button{
        border: 3px solid $primary;
        color: white;
        text-decoration: none;
        font-weight: 600;
        padding: 10px 20px;
        border-radius: 0;
        margin-top: 20px;
    }
}
</style>