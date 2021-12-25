<template>
  <div class="mainsection">
    <div class="container">
      <h2 class="title mainsection__title">Why choose CashForCars to sell your car?</h2>
      <div class=mainsection__tosell>
        <div class="row">
          <div class="col col-1-2 col-tablet">
            <div class='chooseToSell'>
              <p class="chooseToSell__paragraf"
                 v-for='item in chooseToSell'
                 :key='item.id'
              >
                {{item.argument}}
              </p>
            </div>
          </div>
          <div class="col col-1-2 col-tablet">
            <div class="mainsection__col-inner">
            </div>
          </div>
        </div>
      </div>
      <SellCarLists
        :sellList1='sellList1'
        :sellList2='sellList2'
      />
      <div class="row row__inner">
        <div class="col col-1-2 col-tablet">
          <div class="tradeandsell">
            <h2 class="title tradeandsell__title">Trade In</h2>
            <p class="tradeandsell__text">
              Don't let dealers give you less at trade-in, take a look at why
              CashForCars is a great way to get more money for your car! There
              are many great reasons to choose us over a standard dealer trade-in!
            </p>
          </div>
        </div>
        <div class="col col-1-2 col-tablet">
          <div class="tradeandsell">
            <h2 class="title tradeandsell__title">Sell On Your Own</h2>
            <p class="tradeandsell__text">
              Selling a car on your own can be unpredictable and stressful, with
              CashForCars you can sell your car as soon as you're ready. Check
              out why we're better than selling it yourself!
            </p>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col col-1-2 col-tablet">
          <h2 class="title title_customers">
            What our customers<br> have been saying
          </h2>
        </div>
        <div class="col col-1-2 col-tablet">
          <Slider/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SellCarLists from '@/components/SellCarLists.vue'
import Slider from '@/components/Slider.vue'
export default {
  name: 'Mainsection',
  components: {
    SellCarLists,
    Slider
  },
  data () {
    return {
      chooseToSell: [
        {
          id: 1,
          argument: `Advertising your car for sale privately can be a costly, 
                    not to mention frustrating process which is renowned for 
                    attracting time wasters.`
        },
        {
          id: 2,
          argument: `Using CashForCars eliminates the hassle of strangers 
                    visiting your home, the worry associated with them taking a 
                    test drive uninsured and guarantees peace of mind by working 
                    with a reputable company.`
        },
        {
          id: 3,
          argument: `By dealing directly with CashForCars you also eliminate the 
                    worry of cheques bouncing and unsatisfied customers returning 
                    to your door.`
        },
        {
          id: 3,
          argument: `CashForCars is the quick, easy and efficient way to turn 
                    your car into cash for whatever reason. If you are purchasing 
                    a replacement vehicle of a dealer, selling your car to 
                    CashForCars puts you in the driving seat and you will be 
                    able to negotiate a much better deal.`
        }
      ],
      sellList1: [
        {
          id: 1,
          text: 'Sell your car right away'
        },
        {
          id: 2,
          text: 'Secure payment & release of ownership'
        },
        {
          id: 3,
          text: 'Sales are final'
        },
        {
          id: 4,
          text: 'Instant Payment'
        },
        {
          id: 5,
          text: 'No Fees'
        },
        {
          id: 6,
          text: 'No Strangers Visiting Your Home'
        },
        {
          id: 7,
          text: 'No Time Wasters & Tyre Kickers'
        },
        {
          id: 8,
          text: "We'll take your car as it is"
        }
      ],
      sellList2: [
        {
          id: 1,
          text: "We'll take your car as it is"
        },
        {
          id: 2,
          text: 'Cash in hand and more of it'
        },
        {
          id: 3,
          text: 'Transparent and fair appraisal'
        },
        {
          id: 4,
          text: 'Know the price upfront'
        },
        {
          id: 5,
          text: 'Easy and convenient'
        },
        {
          id: 6,
          text: 'Outstanding Finance Settled'
        },
        {
          id: 7,
          text: 'No Bouncing Cheques'
        },
        {
          id: 8,
          text: 'Avoid Uninsured Test Drives'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
.mainsection
  padding-top: 0px
  padding-bottom: 70px
  &__tosell
    margin-bottom: 85px
.mainsection__col-inner
  width: 100%
  height: 299px
  background-image: url('../assets/images/CarsImg.jpg')
  background-position: center
  background-repeat: no-repeat
  background-size: cover
.chooseToSell
  font-weight: normal
  font-size: 16px
  line-height: 26px
  color: #252851
  &__paragraf
    margin-bottom: 20px
    &:last-child
      margin-bottom: 0px
.tradeandsell
  background: #126FB8
  border-radius: 8px
  color: #FFFFFF
  padding: 32px
  &__title
    color: #FFFFFF
    margin-bottom: 14px
    line-height: 32px
  &__text
    font-weight: normal
    font-size: 16px
    line-height: 26px
.row__inner
  margin-bottom: 87px
.title_customers
  line-height: 40px
  margin-bottom: 0
@media (max-width: 376px)
  .mainsection
    padding: 62px 14px 18px 14px
    &__title
      line-height: 40px
      margin-bottom: 25px
    &__tosell
      padding: 0 5px
      margin-bottom: 48px
  .chooseToSell
    margin-bottom: 30px
  .mainsection__col-inner
    width: 100%
    height: 222px
    background-position: center
    background-repeat: no-repeat
    background-size: cover
  .tradeandsell
    padding: 32px 24px
  .row__inner
    margin-bottom: 65px
  .title_customers
    padding-bottom: 8px
</style>
