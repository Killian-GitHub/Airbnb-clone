<template>
  <section class="banner">
      <div class="info">
          <DateSearch />
          <h2>
              Sortez et étendez votre imagination
          </h2>
          <p>Planifiez une escapade pour découvrir les trésors cachés près de chez vous</p>
          <router-link to="/search">
            <button class="info__btn">Explorer à proximité</button>
          </router-link>
      </div>
  </section>
</template>

<script>
import DateSearch from '../components/DateSearch.vue'
export default {
    name: "Banner",
    components: {
        DateSearch
    },
    // data() {
    //     return {
    //         show: false
    //     }
    // }
}
</script>

<style scoped lang="scss">
    .banner {
        background: url("https://media.cntraveler.com/photos/5db1d0dd11c1e500092e7133/master/pass/airbnb-ski-aspen-28328347.jpg") center center;
        height: 380px;
        position: relative;
        h2 {
            font-size: 20px;
            margin-top: 30px;
        }
    }

    .info {
        background-color: rgba(0, 0, 0, 0.8);
        color: white;
        padding: 57px 50px 70px 50px;
        width: 250px;
        .info__btn {
            background-color: #ff7779;
            color: white;
            font-size: 14px;
            font-weight: 600;
            border: none;
            border-radius: 5px;
            padding: 8px 12px;
            margin-top: 15px;
            &:hover {
                cursor: pointer;
                background-color: #fefefe;
                color: #ff7779;
            }
        }
    }
</style>

// https://a0.muscache.com/im/pictures/73b52a62-f4e8-411c-b2a8-125a6e3e59e2.jpg