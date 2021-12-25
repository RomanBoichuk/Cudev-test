<template>
  <div class="row">
    <div class="slider__sellcarlists">
      <Slider1/>
    </div>
    <div class="sellcarlists">
      <div class="row">
        <div class="col col-1-2">
          <ul class=sellcarlists__list>
            <li class=sellcarlists__list-item v-for='item in sellList1' :key="item.id">
              {{item.text}}
            </li>
          </ul>
        </div>
        <div class="col col-1-2">
          <ul class=sellcarlists__list>
            <li class=sellcarlists__list-item v-for='item in sellList2' :key="item.id">
              {{item.text}}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Slider1 from '@/components/Slider1.vue'
export default {
  name: 'SellCarLists',
  components: {
    Slider1
  },
  props: [
    'sellList1',
    'sellList2'
  ]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
.sellcarlists
  padding: 60px 0px 30px 0px
  border-radius: 8px
  background-color: rgba(37,40,81, 0.1)
  text-align: left
  margin-bottom: 66px
.sellcarlists__list
  width: 368px
  margin-left: 96px
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
.slider__sellcarlists
  display: none
@media (max-width: 376px)
  .slider__sellcarlists
    display: block
  .sellcarlists
    display: none
</style>
