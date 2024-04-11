<template>
    <footer id="footer-bottom">
        <div id="socials" class="container d-flex justify-content-between align-items-center ">
            <div>
                <button type="button" class="btn btn-link">SIGN-UP NOW!</button>
            </div>
            <div>
                <ul class="d-flex">
                    <li class="text-uppercase fs-4 fw-bold">Follow us</li>
                    <li><a href="#"><img src="/img/footer-facebook.png" alt="facebook" class="icone-social"></a></li>
                    <li><a href="#"><img src="/img/footer-twitter.png" alt="twitter" class="icone-social"></a></li>
                    <li><a href="#"><img src="/img/footer-youtube.png" alt="youtube" class="icone-social"></a></li>
                    <li><a href="#"><img src="/img/footer-pinterest.png" alt="pinterest" class="icone-social"></a></li>
                    <li><a href="#"><img src="/img/footer-periscope.png" alt="periscope" class="icone-social"></a></li>
                </ul>
            </div>
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

#footer-bottom {
    background-color: #303030;
    height: 110px;
    position: relative;
    margin: 0 auto;

    #socials{
        padding-top: 20px;
        margin: 0 auto;
    }
    button {
        border: 3px solid $primary;
        color: white;
        text-decoration: none;
        font-weight: 600;
        padding: 10px 20px;
        border-radius: 0;
        margin-top: 20px;
        
        &:hover{
            background-color: $primary;
            transform: scale(1.1);
            transition: 0.5s;
        }
    }
    li{
        list-style: none;
        color: $primary;
        padding: 0 10px;
    }

    .icone-social{
        margin: 0 auto;
        
        &:hover{
            cursor: pointer;
            background-color: white;
            transform: scale(1.5);
            transition: 0.5s;
            border-radius: 50%;

        }
    }
}
</style>