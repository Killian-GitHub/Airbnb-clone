<template>
  <section>
      <div class="info">
          <DateSearch />
          <h2>
              Sortez et étendez votre imagination
          </h2>
          <p>Planifiez une escapade pour découvrir les trésors cachés près de chez vous</p>
          <button class="info__btn">Explorer à proximité</button>
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
    section {
        background: url("https://media.cntraveler.com/photos/5db1d0dd11c1e500092e7133/master/pass/airbnb-ski-aspen-28328347.jpg") center center;
        height: 358px;
        position: relative;
        h2 {
            font-size: 20px;
            margin-top: 30px;
        }
    }

    .info {
        background-color: black;
        color: white;
        padding: 45px 50px 60px 50px;
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