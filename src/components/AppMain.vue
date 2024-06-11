<script>
import CurrentSeriesList from './CurrentSeriesList.vue';

export default {
  data() {
    return {
      linksDc: [
        {
            id: 1,
            text: 'digital comics',
            img: "./src/assets/img/buy-comics-digital-comics.png",
        },
        {
            id: 2,
            text: 'dc merchandise',
            img: "./src/assets/img/buy-comics-merchandise.png",
        },
        {
            id: 3,
            text: 'subscription',
            img: "./src/assets/img/buy-comics-subscriptions.png",
        },
        {
            id: 4,
            text: 'comic shop locator',
            img: "./src/assets/img/buy-comics-shop-locator.png",
        },
        {
            id: 5,
            text: 'dc power visa',
            img: "./src/assets/img/buy-dc-power-visa.svg",
        },
      ]
    }
  },
  components: {
    CurrentSeriesList
  }
}
</script>

<template>
    <div class="jumbotron">
        </div>
        <CurrentSeriesList />
        <section class="buy">
            <div class="width-flex">
                <article v-for="article in linksDc" :key="article.id">
                    <img :src="article.img" :alt="article.id">
                    <a href="">{{ article.text.toUpperCase() }}</a>
                </article>
            </div>
        </section>  
</template>



<style lang="scss" scoped>
@use '../styles/partials/variables' as *;



.jumbotron {
        background-image: url(../assets/img/jumbotron.jpg);
        background-size: 100%;
        padding: 12.5rem;
    }

    section.buy {
    background-color: #0282f9;
    padding: 3.2rem;
    z-index: 1;
    position: relative;

    .width-flex {
        display: flex;
        max-width: 1300px;
        margin: 0 auto;
    }

    article {
        width: calc(100% / 5);
        display: flex;
        justify-content: center;
        align-items: center;

        img {
            width: 55px;
            height: 55px;
            object-fit: contain;
        }
    }

    a {
        color: white;
        text-align: center;
        margin-left: 1rem;
    }
}

</style>