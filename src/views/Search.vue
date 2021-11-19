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
  </section>
</template>

<script>
export default {
  name: 'Search'
}
</script>

<style scoped lang="scss">
  .search {
    padding: 20px;
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
      &:hover {
        cursor: pointer;
        border: 1px solid black;
        transition: 0.4s;
      }
    }
  }
</style>