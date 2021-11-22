<template>
    <section class="search">
      <div class="info">
        <p>1 semaine · 24 Décembre 2021 · 2 personnes</p>
        <h2>Logements ⋅ Les Sables D' Olonnes</h2>
        <button class="search__btn">Annulation gratuite</button>
        <button class="search__btn">Type de logement</button>
        <button class="search__btn">Prix</button>
        <button class="search__btn">Réservation instantanée</button>
        <button class="search__btn">Plus de filtres</button>
      </div>
      <SearchResult
        img="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQ_wbPYTxQPMcBh7SPzLFActXnP3uhifeVT_g&usqp=CAU"
        location="Chambre privée · La Chaume - Les Sables-d'Olonne"
        title="Découvrez le quartier des pêcheurs"
        description="1 voyageur · 1 chambre · 1 lit · 1 salle de bain · wifi · cuisine · parking · machine à laver"
        star="4.73"
        comments="8"
      />
      <SearchResult
        img="https://www.expatkings.com/wp-content/uploads/2018/10/Airbnb-rental-tips.-Hostmaker-1-620x349.jpg"
        location="Logement entier : appartement · Les Sables-d'Olonne"
        title="Le luxe à 2 pas de la plage"
        description="2 voyageurs · 2 salles de bains · 2 chambre ·  2 Lits · wifi · cuisine"
        star="4.3"
        comments="8"
      />
      <SearchResult
        img="https://www.smartertravel.com/uploads/2017/07/Untitled-design-8.jpg"
        location="Logement entier : maison · L'Île-d'Olonne "
        title="Le calme à 10 min de la plage"
        description="4 voyageurs · 1 salle de bain · 3 chambre · 3 lits · machine à laver"
        star="3.8"
        comments="8"
      />
      <SearchResult
        img="https://cdn.bisnow.net/fit?height=489&type=jpeg&url=https%3A%2F%2Fs3.amazonaws.com%2Fcdn.bisnow.net%2Fcontent%2Fimages%2F2017%2F05%2F59151d0978bbf_https_press_atairbnb_com_app_uploads_2016_12_midtown_4.jpeg&width=717&sign=FeltIPi9cOWA36nVIeDvZxwgtiCZrpUyMRdvyZviTUI"
        location="Chambre privée · Les Sables-d'Olonne"
        title="Au plus près du Vendée Globe"
        description="2 vouyageur · 1 chambre · 1 lit · 1 salle de bain · wifi · cuisine · parking · machine à laver"
        star="4.1"
        comments="8"
      />
      <SearchResult
        img="https://media.cntraveler.com/photos/5a8f258bd363c34048b35aac/master/w_2250,h_1500,c_limit/airbnb-plus-london.jpg"
        location="Chambre privée · Les Sables-d'Olonne"
        title="À la découverte du centre ville"
        description="2 voyageurs · 1 chambre · 1 lit · 1 salle de bain · wifi · parking"
        star="5.0"
        comments="8"
      />
      <SearchResult
        img="https://image.insider.com/585029a0dd0895bc548b4b8b?width=750&format=jpeg&auto=webp"
        location="Logement entier : appartement · Les Sables-d'Olonne"
        title="Le manoir d'Olonne"
        description="3 voyageurs · 2 chambre · 2 lits · 2 salles de bains · wifi · cuisine · parking · machine à laver"
        star="3.85"
        comments="8"
      />
    </section>
    <aside class="aside">
      <img :src="require('../assets/map-olonne.png')" class="aside__map" alt="map" />
    </aside>
</template>

<script>
import SearchResult from '../components/SearchResult.vue'
export default {
  name: 'Search',
  components: {
    SearchResult,
  }
}
</script>

<style scoped lang="scss">
  @mixin mobile {
    @media screen and (max-width: 750px) {
        @content;
    }
  }
  @mixin desktop {
      @media screen and (max-width: 1200px) {
          @content;
      }
  }
  .search {
    padding: 20px;
    width: 60%;
    @include mobile {
      padding: 0;
    }
    @include desktop {
      width: 100%;
    }
    .info {
      margin: 20px 0 0 20px;
    }
    p {
      font-size: 16px;
      margin-bottom: 5px;
    }
    h2 {
      font-size: 32px;
      margin: 10px 0 15px;
    }
    .search__btn {
      padding: 10px 18px;
      background-color: white;
      border: 1px solid lightgray;
      border-radius: 999px;
      font-size: 14px;
      margin-right: 8px;
      &:nth-child(even) {
        display: none;
      }
      &:hover {
        cursor: pointer;
        border: 1px solid black;
        transition: 0.4s;
      }
    }
  }
  .aside {
    width: 30%;
    position: fixed;
    height: 100vh;
    right: 0;
    top: 0;
    @include desktop {
      display: none;
    }
    &__map {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
</style>