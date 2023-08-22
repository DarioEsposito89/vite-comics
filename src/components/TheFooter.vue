<script>
export default {
    name: 'TheFooter',
    data() {
        return {
            listComic: [
                {
                    name: 'carachters',
                },
                {
                    name: 'comics',
                },
                {
                    name: 'movies',
                },
                {
                    name: 'TV',
                },
                {
                    name: 'games',
                },
                {
                    name: 'videos',
                },
                {
                    name: 'news',
                },
            ],
            listShop: [
                {
                    name: 'shop DC',
                },
                {
                    name: 'shop DC Collectibles',
                },
            ],
            listDC: [
                {
                    name: 'terms of use',
                },
                {
                    name: 'privacy policy (new)',
                },
                {
                    name: 'ad choices',
                },
                {
                    name: 'advertising',
                },
                {
                    name: 'jobs',
                },
                {
                    name: 'subscriptions',
                },
                {
                    name: 'talent',
                },
                {
                    name: 'workshops',
                },
                {
                    name: 'CPSC',
                },
                {
                    name: 'certificates',
                },
                {
                    name: 'ratings',
                },
                {
                    name: 'shop help',
                },
                {
                    name: 'contact us',
                },
            ],
            listSites: [
                {
                    name: 'DC',
                },
                {
                    name: 'MAD',
                },
                {
                    name: 'magazine',
                },
                {
                    name: 'DC kids',
                },
                {
                    name: 'DC',
                },
                {
                    name: 'universe',
                },
                {
                    name: 'DC power visa',
                },
            ],
            listSocial: [
                {
                    img: 'footer-facebook.png',
                },
                {
                    img: 'footer-twitter.png',
                },
                {
                    img: 'footer-youtube.png',
                },
                {
                    img: 'footer-pinterest.png',
                },
                {
                    img: 'footer-periscope.png',
                },
            ]

        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <footer>
        <section class="section-middle">
            <div class="container d-flex justify-content-between align-items-center">
                <div class="list-container d-flex pt-2 gap-5">
                    <div id="comics-and-shop">
                        <h6>DC COMICS</h6>
                        <ul>
                            <li v-for="link in listComic" class="lh-1 text-capitalize">
                                <a href="#">{{ link.name }}</a>
                            </li>
                        </ul>

                        <h6>SHOP</h6>
                        <ul>
                            <li v-for="link in listShop" class="lh-1 text-capitalize">
                                <a href="#">{{ link.name }}</a>
                            </li>
                        </ul>
                    </div>
                
                    <div id="dc">
                        <h6>DC</h6>
                        <ul>
                            <li v-for="link in listDC" class="lh-1 text-capitalize">
                                <a href="#">{{ link.name }}</a>
                            </li>
                        </ul>
                    </div>
                
                    <div id="SITES">
                        <h6>SITES</h6>
                        <ul>
                            <li v-for="link in listSites" class="lh-1 text-capitalize">
                                <a href="#">{{ link.name }}</a>
                            </li>
                        </ul>
                    </div>
                </div>

                <div class="big-logo">
                    <img src="/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </section>
        
        <section class="section-bottom d-flex align-items-center">
            <div class="container d-flex justify-content-between align-items-center">
                <div class="sign">
                    <button type="button" class="btn btn-outline-primary rounded-0 text-white">SIGN-UP NOW!</button>
                </div>

                <div class="follow d-flex">
                    <h3 class="text-primary">FOLLOW US</h3>
                    <ul class="list-social d-flex gap-3">
                        <li v-for="social in listSocial">
                            <a href="#" class="me-5">
                                <div class="img-container">
                                    <img :src="getImagePath(`/img/${social.img}`)" alt="">
                                </div>
                            </a> 
                        </li>
                    </ul>
                </div>
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>

.section-middle {
    background: url("/img/footer-bg.jpg");
    background-size: cover;
    height: 500px;
    overflow: hidden;
}

.container {
    .list-container {
        width: 50%;

        >div{
            
            h6 {
                color: white;
                margin: 0.5rem 0;
            }

            ul {
                padding: 0;
            }

            a {
                color: rgb(173, 168, 168);
                font-size: 10px;
                margin: 1rem 0;
            }
        }
    }

}

/* inizio section bottom */
.section-bottom {
    height: 100px;
    background-color: #303030;

    .container {
        height: 100%;
    }
}
</style>