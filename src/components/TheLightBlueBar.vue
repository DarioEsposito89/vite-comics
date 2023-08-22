<script>
export default {
    name: 'TheLightBlueBar.vue',
    data() {
        return {
            linksBuy: [
                {
                    img: 'buy-comics-digital-comics.png',
                    name: 'Digital Comics',
                },
                {
                    img: 'buy-comics-merchandise.png',
                    name: 'Dc Merchandise',
                },
                {
                    img: 'buy-comics-subscriptions.png',
                    name: 'SubscriptionS',
                },
                {
                    img: 'buy-comics-shop-locator.png',
                    name: 'Comic shop locator',
                    resize: 'special-img',
                },
                {
                    img: 'buy-dc-power-visa.svg',
                    name: 'Dc power Visa',
                },
            ],
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
    <section class="section-top">
        <div class="container">
            <ul class="list-buy d-flex justify-content-between align-items-cemter gap-3">
                <li v-for="link in linksBuy" class="text-uppercase d-flex align-items-center">
                    <a href="#" class="text-white d-flex gap-3 align-items-center">
                            <img :src="getImagePath(`/img/${link.img}`)" alt="">
                            {{ link.name }}
                    </a>
                </li>
            </ul>
        </div>
    </section> 
</template>

<style lang="scss" scoped>
// /* section top */
.section-top{
    background-color: rgb(0, 128, 255);
    position: sticky;
    top: 0;
    z-index: 1;

    .container{
        height: 130px;

        > .list-buy{
            height: 100%;
                li > a{
                
                > img{
                    width: 50px;
                    height: 55px;
                }
            }
        }
    }

}
</style>