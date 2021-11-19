<template>
  <footer>
      <p>Clone Airbnb © 2021 - Aucun droit réservé - ceci est une démo !</p>
      <p>Confidentialité · Conditions · Détails de l'entreprise</p>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped lang="scss">
  footer {
    border-top: 1px solid lightgray;
    padding: 10px;
    background-color: #f7f7f7;
    bottom: 0;
    text-align: center;
    p {
      padding: 5px;
      font-size: 14px;
    }
  }
</style>