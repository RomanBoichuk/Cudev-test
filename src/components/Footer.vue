<template>
  <div class="footer">
    <div class="container">
      <div class="footer__inner">
        <div class="menu">
          <ul class="menu__list">
            <li class="menu__item" v-for='item in navBarMenu' :key='item'>
              <a class="menu__link" href=#> {{item}} </a>
            </li>
          </ul>
        </div>
        <img class=login__img :src=" require('../assets/cfclogo1.png')" alt="item">
      </div>
      <div class="footer__description">
        <p class="footer__description--text">
          ©2021 Cash for Cars  |  Terms and Conditions  |  Privacy Policy
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
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
.footer
  max-width: 1440px
  margin-left: auto
  margin-right: auto
  background: linear-gradient(0deg, #252851, #252851)
  padding: 59px 0px 60px
.footer__inner
  display: flex
  justify-content: space-between
  align-items: center
.menu__list
  display: flex
.menu__item
  margin-left: 32px
  &:first-child
    margin-left: 0px
.menu__link
  color: #FFFFFF
  text-decoration: none
  font-size: 16px
  line-height: 22px
  text-align: right
.footer__description
  margin-top: 26px
  &--text
    font-weight: normal
    font-size: 12px
    line-height: 17px
    color: #126FB8
@media (max-width: 376px)
  .footer
    padding: 42px 35px 35px 71px
    &__inner
      flex-wrap: wrap
  .menu
    margin-right: auto
    margin-left: auto
    margin-bottom: 28px
  .menu__list
    flex-direction: column
  .menu__item
    margin-left: 32px
    margin-bottom: 16px
    &:first-child
      margin-left: 32px
    &:last-child
      margin-bottom: 0
  .footer__description
    text-align: center
    &--text
      padding-left: 5px
      padding-right: 5px
</style>
