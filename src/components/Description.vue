<template>
  <div class="description">
    <div class="container">
      <div class="description__inner">
        <h2 class="title description__title--adaptiv">We Pay Cash For Cars</h2>
        <div class="description__content">
          <p class="description__content--text">
            CashForCars is the safe, easy and cost effective alternative to selling
            your car to a dealer or through private advertisement. We guarantee to
            buy your car whatever the make, age, model or condition. No hassle, no
            time wasters, no bouncing cheques and no fees. Sell your car in Belfast
            today!<br><br>
            We operate from premises in the Belfast area and will buy cars throughout Northern Ireland.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Description'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
.description
  max-width: 1440px
  margin-left: auto
  margin-right: auto
  padding: 91px 0 42px 0
  &__inner
    text-align: center
.description__content
  max-width: 760px
  margin-left: auto
  margin-right: auto
  &--text
    font-weight: normal
    font-size: 16px
    line-height: 24px
    color: #252851
@media (max-width: 376px)
  .description
    padding: 46px 14px 66px 14px
    &__inner
      text-align: left
    &__title--adaptiv
      font-size: 32px
      line-height: 40px
      margin-right: 118px
</style>
