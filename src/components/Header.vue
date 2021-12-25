<template>
  <div class="header">
    <div class="container">
      <div class="header__inner">
        <img class=login__img :src=" require('../assets/cfclogo1.png')" alt="item">
        <div class="menu">
          <button class="menu__btn">
            <span><font-awesome-icon icon="bars"/></span>
          </button>
          <ul class="menu__list">
            <li class="menu__item" v-for='item in navBarMenu' :key='item'>
              <a class="menu__link" href=#> {{item}} </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      navBarMenu: [
        'Hot it works',
        'Why choose us',
        'FAQs',
        'Contact'
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
.header
  max-width: 1440px
  height: 104px
  margin-left: auto
  margin-right: auto
  background: #252851
.header__inner
  display: flex
  justify-content: space-between
  align-items: center
  padding: 24px 0px 23px
.menu__btn
  display: none
  width: 24px
  height: 18px
  color: #FFFFFF
  span
    width: 24px
    height: 18px
.menu__list
  display: flex
.menu__item
  margin-left: 32px
.menu__link
  color: #FFFFFF
  text-decoration: none
  font-size: 16px
  line-height: 22px
  text-align: right
@media (max-width: 376px)
  .menu__btn
    display: block
  .menu__list
    display: none
</style>
