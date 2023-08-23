<script>
export default{
    name: 'TheCards',
    props: {
        title: String,
        src: String,
    }
}
</script>

<template>
    <div>
        <div class="img-series">
            <a href="#"><img :src="src" :alt="title"></a>
        </div>
        <p class="text-white text-uppercase pt-2">{{ title }}</p>
    </div>
</template>

<style lang="scss" scoped>
.card{
    width: calc(100% / 6);
    padding: 10px;
    padding-bottom: 30px ;
    background-color:rgb(27, 27, 27);
    border: 0;
}
.img-series{
    width: 100%;

    img{
        width: 100%;
        height: 180px;
        object-fit: cover;
        object-position: top;
    }

}
</style>