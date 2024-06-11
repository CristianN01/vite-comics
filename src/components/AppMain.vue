<script>
import CurrentSeriesList from './CurrentSeriesList.vue';

export default {
  data() {
    return {
      
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
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;



.jumbotron {
        background-image: url(../assets/img/jumbotron.jpg);
        background-size: 100%;
        padding: 12.5rem;

        // img {
        //     width: 100%;
        //     background-repeat: no-repeat;
        //     height: 200px;
        //     object-fit: cover;
        // }
    }

</style>