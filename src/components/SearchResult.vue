<template>
  <div class="search-result">
      <img :src="img" alt="">
      <i class="far fa-heart heart" />
      <div class="info">
          <div class="info__top">
              <p>{{location}}</p>
              <h3>{{title}}</h3>
              <p>___</p>
              <p>{{description}}</p>
          </div>
          <div class="info__bottom">
              <div class="rated">
                  <i class="fas fa-star star" />
                  <p><strong>{{star}}</strong></p>
              </div>
              <p class="comments">({{comments}} commentaires)</p>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'SearchResult',
    props: {
        img: String,
        location: String,
        title: String,
        description: String,
        star: String,
        comments: String,
    }
}
</script>

<style scoped lang="scss">
@mixin mobile {
    @media screen and (max-width: 750px) {
        @content;
    }
}
.search-result {
    display: flex;
    margin: 30px auto;
    padding: 0 0 30px;
    border-bottom: 1px solid lightgray;
    cursor: pointer;
    @include mobile {
        flex-direction: column;
        padding: 25px;
        margin: 0;
    }
    &:hover {
        opacity: 0.8;
    }
    img {
        height: 220px;
        width: 320px;
        border-radius: 10px;
        overflow: hidden;
        object-fit: cover;
        @include mobile {
            width: 100%;
            height: 350px;
            border: solid 1px lightgray;
        }
    }
    .heart {
        position: absolute;
        right: 20px;
        padding: 10px;
        font-size: 22px;
        @include mobile {
            margin: 10px 13px;
            border-radius: 50%;
            background-color: rgb(247, 247, 247);
        }
        &:hover {
            cursor: pointer;
            border-radius: 50%;
            background-color: rgb(247, 247, 247);
        }
    }
    .info {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        margin-left: 20px;
        @include mobile {
            margin-left: 0;
        }
        &__top {
            width: 40vw;
            p {
                margin-bottom: 10px;
                margin-top: 2px;
                font-size: 14px;
                color: rgb(113, 113, 113);
                @include mobile {
                    color: black;
                    font-size: 19px;
                    width: max-content;
                    margin: 10px 0 0;
                    &:nth-child(1n + 2) {
                        display: none;
                    }
                }
            }
            h3 {
                margin: 0;
                @include mobile {
                    display: none;
                }
            }
        }
        &__bottom {
            display: flex;
            @include mobile {
                margin-top: -10px;
            }
        }
        .rated {
            display: flex;
            align-items: end;
            p {
                font-size: 14px;
                padding-top: 2px;
                margin-bottom: 0;
            }
        }
        .star {
            color: red;
            font-size: 14px;
            margin-right: 5px;
        }
        .comments {
            font-size: 15px;
            color: rgb(113, 113, 113);
            padding-top: 3px;
            margin-left: 5px;
            margin-bottom: -1px;
        }
    }
}

</style>