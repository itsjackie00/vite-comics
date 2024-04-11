<template>
    <footer id="footer-middle">
        <div class="footer-container container">
            <div id="left">
            <div class="row py-2 w-100">
                    <MenuComponents title="DC COMICS" :items="linksFooter.COMICS" />
                    <MenuComponents title="DC" :items="linksFooter.DC" />
                    <MenuComponents title="SITES" :items="linksFooter.SITES" />
                    <MenuComponents title="SHOP" :items="linksFooter.SHOP" />
                </div>
            </div>
            <div class="image-container"id="right">
                <img src="/img/dc-logo-bg.png" alt="DC logo" >
            </div>
        </div>
    </footer>
</template>

<script>
import MenuComponents from './MenuComponents.vue';

export default {
    name: 'FooterComponentMiddle',
    components: {
        MenuComponents
    },
    data() {
        return {
            linksFooter: {
                COMICS: [
                    {
                        text: 'Characters',
                        url: '#'
                    },
                    {
                        text: 'Comics',
                        url: '#'
                    },
                    {
                        text: 'Movies',
                        url: '#'
                    },
                    {
                        text: 'TV',
                        url: '#'
                    },
                    {
                        text: 'Games',
                        url: '#'
                    },
                    {
                        text: 'Videos',
                        url: '#'
                    },
                    {
                        text: 'News',
                        url: '#'
                    }
                ],
                SHOP: [
                    {
                        text: 'Shop DC',
                        url: '#'
                    },
                    {
                        text: 'Shop DC Collectibles',
                        url: '#'
                    }
                ],
                DC: [
                    {
                        text: 'Terms Of Use',
                        url: '#'
                    },
                    {
                        text: 'Privacy policy (New)',
                        url: '#'
                    },
                    {
                        text: 'Ad Choices',
                        url: '#'
                    },
                    {
                        text: 'Advertising',
                        url: '#'
                    },
                    {
                        text: 'Jobs',
                        url: '#'

                    },
                    {
                        text: 'Subscriptions',
                        url: '#'
                    },
                    {
                        text: 'Talent Workshops',
                        url: '#'
                    },
                    {
                        text: 'CPSC Certificates',
                        url: '#'
                    },
                    {
                        text: 'Ratings',
                        url: '#'
                    },
                    {
                        text: 'Shop Help',
                        url: '#'
                    },
                    {
                        text: 'Contact Us',
                        url: '#'
                    },
                ],
                SITES: [
                    {
                        text: 'DC',
                        url: '#'
                    },
                    {
                        text: 'MAD Magazine',
                        url: '#'
                    },
                    {
                        text: 'DC Kids',
                        url: '#'
                    },
                    {
                        text: 'DC Universe',
                        url: '#'
                    },
                    {
                        text: 'DC Power Visa',
                        url: '#'
                    }
                ]
            }
        }
    }

}
</script>

<style lang="scss" scoped>
#footer-middle {
    background-image: url('/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    color: white;
    width: 100%;

    .footer-container {
        display: flex;
        justify-content: space-between;
        align-items: center;

        #left,
        #right {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100%;
        }

        #left {
            width: 45%;
        }

        #right {
            width: 65%;

            img {
                position: absolute;
                width: 700px;
                overflow: hidden;

            }
        }
    }

}

/* ==== MEDIA QUERY ==== */
@media screen and (max-width: 768px) {
    #footer-middle .footer-container #right img {
        width: 400px;
    }
}
</style>