<template>
  <div class="slider middle">
    <div class="slides">
      <input type="radio" name="r" id="r1">
      <input type="radio" name="r" id="r2">
      <input type="radio" name="r" id="r3">
      <input type="radio" name="r" id="r4">
      <div class="slide s1">
        <p class="slide__text">
          "Can't recommend them enough. Their fast, friendly service was ideal, and they offered us a better price than other trade in sites..."
        </p>
      </div>
      <div class="slide">
        <p class="slide__text">
          "22222222 Can't recommend them enough. Their fast, friendly service was ideal, and they offered us a better price than other trade in sites..."
        </p>
      </div>
      <div class="slide">
        <p class="slide__text">
          "333333333 Can't recommend them enough. Their fast, friendly service was ideal, and they offered us a better price than other trade in sites..."
        </p>
      </div>
      <div class="slide">
        <p class="slide__text">
          "44444444444 Can't recommend them enough. Their fast, friendly service was ideal, and they offered us a better price than other trade in sites..."
        </p>
      </div>
    </div>
    <div class="navigation">
      <label for="r1" class="bar"></label>
      <label for="r2" class="bar"></label>
      <label for="r3" class="bar"></label>
      <label for="r4" class="bar"></label>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Slider'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
.slider
  width: 496px
  height: 280px
  overflow: hidden
  position: relative
.navigation
  position: absolute
  margin-top: 12px
  bottom: 12px
  left: 90%
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
input[name='r']
  position: absolute
  visibility: hidden
.slides
  width: 400%
  height: 248px
  display: flex
.slide
  width: 25%
  transition: all 0.4s ease
  padding: 48px 64px
  display: flex
  align-items: center
  background: rgba(18, 111, 184, 0.1)
  border-radius: 8px
  &__text
    font-weight: normal
    font-size: 24px
    line-height: 38px
    letter-spacing: -0.01em
#r1:checked ~ .s1
  margin-left: 0
#r2:checked ~ .s1
  margin-left: -25%
#r3:checked ~ .s1
  margin-left: -50%
#r4:checked ~ .s1
  margin-left: -75%
@media (max-width: 376px)
  .slider
    width: 100%
    height: 180px
  .navigation
    left: 50%
    bottom: 0
  .slides
    height: 152px
  .slide
    padding: 24px
    &__text
      font-size: 16px
      line-height: 26px
</style>
