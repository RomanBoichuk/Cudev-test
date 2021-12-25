<template>
  <div class="slider middle">
    <div class="slides">
      <input type="radio" name="k" id="k1">
      <input type="radio" name="k" id="k2">
      <div class="slide s1">
        <ul class=sellcarlists__list>
          <li class=sellcarlists__list-item v-for='item in sellList1' :key="item.id">
            {{item.text}}
          </li>
        </ul>
      </div>
      <div class="slide">
        <ul class=sellcarlists__list>
          <li class=sellcarlists__list-item v-for='item in sellList2' :key="item.id">
            {{item.text}}
          </li>
        </ul>
      </div>
    </div>
    <div class="navigation">
      <label for="k1" class="bar"></label>
      <label for="k2" class="bar"></label>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Slider',
  data () {
    return {
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
.slider
  width: 327px
  height: 436px
  overflow: hidden
  position: relative
.navigation
  position: absolute
  margin-top: 12px
  bottom: 0
  left: 50%
  transform: translateX(-50%)
  display: flex
.bar
  width: 12px
  height: 12px
  margin-left: 12px
  background: rgba(18, 111, 184, 0.1)
  border-radius: 50%
  transition: all 0.4s ease
  &:hover
    background: #126FB8
input[name='k']
  position: absolute
  visibility: hidden
.slides
  width: 200%
  height: 408px
  display: flex
.slide
  width: 50%
  text-align: left
  transition: all 0.4s ease
  padding: 28px 24px
  display: flex
  align-items: center
  background: rgba(18, 111, 184, 0.1)
  border-radius: 8px
  &__text
    font-weight: normal
    font-size: 24px
    line-height: 38px
    letter-spacing: -0.01em
#k1:checked ~ .s1
  margin-left: 0
#k2:checked ~ .s1
  margin-left: -50%
.sellcarlists
  padding: 60px 0px 30px 0px
  border-radius: 8px
  background-color: rgba(37,40,81, 0.1)
  text-align: left
  margin-bottom: 66px
.sellcarlists__list
  width: 100%
  margin-left: 32px
.sellcarlists__list-item
  position: relative
  font-weight: bold
  font-size: 16px
  line-height: 24px
  margin-bottom: 15px
  color: #252851
  &:last-child
    margin-bottom: 0px
  &::before
    content: ''
    position: absolute
    width: 16px
    height: 16px
    background: #F7C548
    border-radius: 56px
    top: 50%
    transform: translateY(-50%)
    left: -10%
  &::after
    content: ''
    position: absolute
    border: 4px solid #fff
    width: 2px
    height: 7px
    top: 50%
    transform: translateY(-58%) rotate(-135deg)
    left: -8.5%
    border-right: 0
    border-bottom: 0
    bottom: 2px
</style>
