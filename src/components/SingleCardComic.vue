<script>
export default {
  data() {
    return {
      
    }
  },
  props: {
    singleCardComic: {
        type: Object,

    }
  }
}
</script>

<template>
    <article>
        <img :src="singleCardComic.thumb" :alt="singleCardComic.series">
            <h4>
                {{ singleCardComic.series.toUpperCase() }}
            </h4>
    </article>
</template>


<style lang="scss" scoped>
    article {
            width: calc((100% / 6) - 1rem);
            color: white;
            margin-left: 1rem;
            margin-bottom: 3rem;
           

            h4 {
                margin-top: 1rem;
                font-weight: 200;
            }
            

            img {
                width: 185px;
                height: 185px;
                object-fit: cover;

            }
        }
</style>