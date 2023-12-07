<script>
export default {
  name: 'PictureCard',

  data() {
    return {
      likeCountFirstImg: 0,
      likeCountSecondImg: 0,
      likeCountThirdImg: 0
    }
  },
  methods: {
    addLikeFirstImg() {
      this.likeCountFirstImg++
    },
    addLikeSecondImg() {
      this.likeCountSecondImg++
    },
    addLikeThirdImg() {
      this.likeCountThirdImg++
    },
    deleteLikeFirstImg() {
      if (this.likeCountFirstImg > 0) {
        this.likeCountFirstImg--
      }
    },
    deleteLikeSecondImg() {
      if (this.likeCountSecondImg > 0) {
        this.likeCountSecondImg--
      }
    },
    deleteLikeThirdImg() {
      if (this.likeCountThirdImg > 0) {
        this.likeCountThirdImg--
      }
    }
  }
}
</script>

<template>
  
  <section class="container">
    <div class = "row">
      <div class="col">
        <p class="text-center">
          Mon premier projet en VueJS consiste à créer une galerie d'image et à tester le nombre de cliques sur le bouton "Like".
        </p>
      </div>
    </div>
    <div class="row d-flex align-items-center">
      <div class="col-lg-4 col-sm-12">
        <div class="card d-flex justify-content-center align-items-center shadow p-2">
          <img src="/src/assets/img/bts_img_01.png" alt="Groupe BTS" width="300" />
          <div class="card-body">
            <h5 class="card-title">Image BTS</h5>
            <p class="card-text">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
              incididunt ut labore et dolore magna aliqua.
            </p>
            <div class="card-footer d-flex justify-content-center align-items-center p-1">
              <button type="button" class="btn btn-success me-3" @click.prevent="addLikeFirstImg">
                Like 👍
              </button>
              <button type="button" class="btn btn-outline-danger me-3" @click.prevent="deleteLikeFirstImg">
                Dislike 👎
              </button>
              <span> {{ likeCountFirstImg }} like </span>
            </div>
          </div>
        </div>
      </div>

      <div class="col-lg-4 col-sm-12">
        <div class="card d-flex justify-content-center align-items-center shadow p-2">
          <img src="/src/assets/img/bts_img_02.png" alt="Groupe BTS" width="300" />
          <div class="card-body">
            <h5 class="card-title">Image BTS</h5>
            <p class="card-text">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
              incididunt ut labore et dolore magna aliqua.
            </p>
            <div class="card-footer d-flex justify-content-center align-items-center p-1">
              <button type="button" class="btn btn-success me-3" @click.prevent="addLikeSecondImg">
                Like 👍
              </button>
              <button type="button" class="btn btn-outline-danger me-3" @click.prevent="deleteLikeSecondImg">
                Dislike 👎
              </button>
              <span> {{ likeCountSecondImg }} like </span>
            </div>
          </div>
        </div>
      </div>

      <div class="col-lg-4 col-sm-12">
        <div class="card d-flex justify-content-center align-items-center shadow p-2">
          <img src="/src/assets/img/bts_img_03.png" alt="Groupe BTS" width="300" />
          <div class="card-body">
            <h5 class="card-title">Image BTS</h5>
            <p class="card-text">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
              incididunt ut labore et dolore magna aliqua.
            </p>
            <div class="card-footer d-flex justify-content-center align-items-center p-1">
              <button type="button" class="btn btn-success me-3" @click.prevent="addLikeThirdImg">
                Like 👍
              </button>
              <button type="button" class="btn btn-outline-danger me-3" @click.prevent="deleteLikeThirdImg">
                Dislike 👎
              </button>
              <span> {{ likeCountThirdImg }} like </span>
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<style scoped>
  .card.d-flex.justify-content-center.align-items-center.shadow.p-2{
    background-color: #e8ebe8;
  }
</style>
