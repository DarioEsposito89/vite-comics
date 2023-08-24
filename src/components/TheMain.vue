<script>
import TheCards from './TheCards.vue';
export default {
    name: 'TheMain',
    components:{
        TheCards,
    },
    data() {
        return {
            listCards: [
                {
                    "thumb": "https://www.morawa.at/annotstream/9783741617393/COPL/Johns-Geoff/Superman-Action-Comics-1000-Deluxe-Edition.jpg?sq=3",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://cdn.swiatksiazki.pl/media/catalog/product/6/7/6799906984767-3.jpg?width=350&height=350&store=default&image-type=small_image",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.washingtonpost.com/wp-apps/imrs.php?src=http://www.washingtonpost.com/news/comic-riffs/wp-content/uploads/sites/15/2017/06/AQM_Cv25_ds.jpg&w=1440",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://oyster.ignimgs.com/wordpress/stg.ign.com/2014/12/Batgirl.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://pictures.abebooks.com/isbn/9781401237783-it.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://s3.amazonaws.com/comicgeeks/comics/covers/large-1378337.jpg?1631741515",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.previewsworld.com/SiteImage/MainImage/STL127547",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://m.media-amazon.com/images/I/51galZVEAtL.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://m.media-amazon.com/images/I/41nGyVF7C2L.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://m.media-amazon.com/images/I/512tsmX-SfL.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://m.media-amazon.com/images/I/91uTUXN0sNS._AC_UF1000,1000_QL80_.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://m.media-amazon.com/images/I/912D1VcX40L._AC_UF1000,1000_QL80_.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ],
        }
    }

}
</script>

<template>
    <main>
        <div class="jumbotron">
            <img src="/img/jumbotron.jpg" alt="">
        </div>

        <div class="container">
            <h1 class="text-white">CURRENT SERIES</h1>

            <div class="cards">
                <TheCards class="card" v-for="card in listCards" 
                :key="`card_$(i)`"
                :src="card.thumb" 
                :title="card.series" />
            </div>

            <div class="load">
                <button><a href="#" class="text-white fw-bold">LOAD MORE</a></button>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    background-color: rgb(27, 27, 27);

    .jumbotron {
        height: 500px;

        >img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
        }
    }

    .container {
        position: relative;
        color:dark;

        h1 {
            height: 40px;
            line-height: 40px;
            padding: 0 20px;
            font-size: 1em;
            background-color: rgb(0, 128, 255);
            position: absolute;
            top: -20px;
            left: 0;
        }

        >.cards {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            padding-top: 25px;
        }

        >.load {
            text-align: center;
            padding-bottom: 20px;

            >button {
                background-color: rgb(0, 128, 255);
                border: none;
                padding: 5px 40px;

            }
        }
    }
}
</style>