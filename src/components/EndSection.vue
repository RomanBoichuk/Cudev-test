<template>
  <div class="endsection">
    <div class="container">
      <div class="endsection__inner">
        <h2 class="title endsection__inner--title">Receive your free valuation now</h2>
        <button class="btn">Get Started <span class="btn_icon"><font-awesome-icon icon="arrow-alt-circle-right"/></span></button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Content'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
.endsection
  max-width: 1440px
  margin-left: auto
  margin-right: auto
  padding: 65px 0 65px 0
  background: linear-gradient(247.8deg, #126FB8 0%, #252851 100%)
  &__inner
    display: flex
    flex-direction: column
    align-items: center
    &--title
      color: #FFFFFF
      font-weight: 800
      line-height: 40px
      text-align: center
      margin-bottom: 32px
.btn
  background: #F7C548
  box-shadow: 0px 4px 8px rgba(37, 40, 81, 0.1)
  border-radius: 46px
  padding: 15px 134px 15px 132px
  font-weight: bold
  font-size: 18px
  line-height: 18px
  text-align: center
  color: #252851
@media (max-width: 376px)
  .endsection
    padding: 40px 14px 48px 14px
    &__inner
      &--title
        margin-bottom: 24px
    .btn
      padding-right: 92px
      padding-left: 92px
</style>
