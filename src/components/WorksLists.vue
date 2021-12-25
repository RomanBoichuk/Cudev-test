<template>
  <div class="workslists">
    <div class="row">
      <div class="col col-1-3 col-tablet" v-for="(article, index) in colomn_description" :key="article._id">
        <div class="col-1-3__inner">
          <img class="workslists__picture" alt="PICTURE" :src="article.img">
          <p class="workslists__title">
            <span>
              {{index + 1}}.
            </span>
            {{article.title}}
          </p>
          <p class="workslists__text">{{article.text}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'WorksLists',
  props: [
    'colomn_description'
  ]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
.workslists
  text-align: left
  &__picture
    width: 64px
    height: 64px
    margin-bottom: 29px
    background: #F7C548
    border-radius: 100px
  &__title
    font-weight: bold
    font-size: 24px
    line-height: 24px
    margin-bottom: 14px
  &__text
    font-weight: normal
    font-size: 16px
    line-height: 26px
.col-1-3__inner
  max-width: 320px
@media (max-width: 376px)
  .workslists
    text-align: center
</style>
