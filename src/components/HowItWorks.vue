<template>
  <div class="section2">
    <div class="section2__content">
      <div class="container">
        <div class="section2__inner">
          <h2 class="section2__title">How it works</h2>
          <p class="section2__text">
            It's so easy to sell your car with CashForCars!
          </p>
          <WorksLists
            :colomn_description="articles"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import WorksLists from '@/components/WorksLists.vue'
export default {
  name: 'HowItWorks',
  components: {
    WorksLists
  },
  data () {
    return {
      articles: [
        {
          _id: 1,
          img: '/img/picture/forms.png',
          title: 'Enter Your Details',
          text: 'It takes just a few minutes to complete a form providing us with details of your vehicle. Answer a few questions about your cars mileage, age, condition, etc and fill in your personal details.'
        },
        {
          _id: 2,
          img: '/img/picture/finance 1.png',
          title: 'Receive a Price',
          text: 'We will contact you within 24hrs. If you are satisfied with our valuation we will arrange for you to meet at our premises or for a member of the CashForCars team to visit you.'
        },
        {
          _id: 3,
          img: '/img/picture/carkey.png',
          title: 'Sell Your Car',
          text: 'Once you have met a member of our team the whole process should be concluded within 15–20 minutes. We will pay you by draft cheque or transfer the money securely by Faster Payments there and then, with no fees.'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
.section2
  max-width: 1440px
  margin-left: auto
  margin-right: auto
  color: #FFFFFF
  height: 1010px
  position: relative
  &__inner
    text-align: center
    transform: skewY(5deg)
  &__content
    max-width: 1440px
    margin-left: auto
    margin-right: auto
    padding: 152px 0 155px 0
    background: linear-gradient(247.8deg, #126FB8 0%, #252851 100%)
    transform: skewY(-5deg)
    position: absolute
    left: 0
    right: 0
    top: 67px
.section2__title
  font-weight: bold
  font-size: 32px
  line-height: 32px
  margin-bottom: 27px
.section2__text
  font-size: 24px
  line-height: 36px
  margin-bottom: 71px
@media (max-width: 376px)
  .section2
    height: 1165px
    &__content
      padding: 67px 14px 41px 14px
      top: 16px
  .section2__text
    margin-bottom: 39px
    font-weight: normal
</style>
