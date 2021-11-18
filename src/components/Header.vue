<template>
  <header>
      <i class="fab fa-airbnb logo" />
      <div class="search">
        <input type="text" placeholder="Commencez votre recherche">
        <i class="fas fa-search search__logo"/>
      </div>
      <div class="menu">
        <p>Devenez hôte</p>
        <i class="fas fa-globe globe"></i>
        <div class="dropDown">
          <i class="fas fa-bars bars"></i>
          <i class="fas fa-user-circle avatar"></i>
        </div>
      </div>
  </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style scoped lang="scss">
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: sticky;
  top: 0;
  background-color: #fefefe;
  z-index: 100;
  width: 100%;
  padding: 15px 0;
  box-shadow: 0 1px 8px -2px lightgray;
  .logo {
    font-size: 40px;
    margin-left: 40px;
    color: rgb(252, 28, 74);
    @media screen and (max-width: 740px) {
      display: none;
    }
  }
  .search {
    display: flex;
    align-items: center;
    flex: 1;
    max-width: fit-content;
    height: 22px;
    padding: 12px 6px 12px 12px;
    border: 1px solid lightgray;
    border-radius: 999px;
    box-shadow: 1px 1px 4px lightgray;
    @media screen and (max-width: 740px) {
      margin: 0 auto;
    }
    @media screen and (min-width: 950px) {
      margin-left: 16%;
    }
    input {
      border: none;
      width: 220px;
      padding-left: 12px;
      font-size: 14px;
      outline: none;
      cursor: pointer;
      &::placeholder {
        color: black;
      }
    }
    &__logo {
      font-size: 12px;
      color: #fefefe;
      padding: 11px;
      border-radius: 50%;
      background-color: rgb(252, 28, 74);
    }
    &:hover {
        cursor: pointer;
        box-shadow: 1px 3px 4px lightgray;
        transition: 0.3s;
      }
  }
  .menu {
    display: flex;
    align-items: center;
    justify-content: space-around;
    width: 260px;
    margin-right: 40px;
    @media screen and (max-width: 740px) {
      display: none;
    }
    p {
      font-size: 15px;
      padding: 12px 20px;
      margin: 0;
      color: rgb(52, 51, 52);
      &:hover {
      cursor: pointer;
      background-color: rgb(247, 247, 247);
      border-radius: 999px;
      }
    }
    .globe {
      padding: 14px;
      margin-right: 5px;
      color: rgb(52, 51, 52);
      &:hover {
        cursor: pointer;
        background-color: rgb(247, 247, 247);
        border-radius: 50%;
      }
    }
    .dropDown {
      border: solid 1px lightgray;
      display: flex;
      align-items: center;
      justify-content: space-between;
      width: 52px;
      padding: 5px 5px 5px 15px;
      border-radius: 999px;
      .bars {
        font-size: 14px;
        color: rgb(70, 70, 70);
      }
      .avatar {
        font-size: 30px;
        color: rgb(113, 113, 113);
      }
      &:hover {
        cursor: pointer;
        box-shadow: 1px 2px 4px lightgray;
        transition: 0.3s;
      }
    }
  }
}
</style>