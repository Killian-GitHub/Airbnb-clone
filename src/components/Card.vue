<template>
  <div class="card">
      <img :src="src" alt="">
      <div class="info">
          <h2>{{title}}</h2>
          <h4>{{description}}</h4>
          <h3>{{price}}</h3>
      </div>
  </div>
</template>

<script>
export default {
    props: {
        src: String,
        title: String,
        description: String,
        price: Number
    }
}
</script>

<style scoped lang="scss">
    .card {
        margin: 10px;
        border-radius: 10px;
        overflow: hidden;
        box-shadow: 0px 6px 18px -9px rgba(0, 0, 0, 0.75);
        transition: transform 0.1s ease-in;
        cursor: pointer;
        &:hover {
            transform: scale(1.07);
        }
        img {
            object-fit: fill;
            min-width: 300px;
            min-height: 200px;
            width: 100%;
        }
        .info {
            margin-top: -9px;
            border-radius: 10px;
            padding: 20px;
            border: 1;
            h2 {
                font-size: 18px;
            }
            h4 {
                font-size: 14px;
                margin: 8px auto;
            }
            h3 {
                font-size: 17px;
            }
        }
    }
</style>