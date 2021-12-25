<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="sass">

$siteWidth: 1440
$gap: 10
$vstep: 30

$breakpoints: ('small':  375px, 'medium': 530px, 'large': 1440px) !default
@mixin respond-to($breakpoint)
  @if map-has-key($breakpoints, $breakpoint)
    @media (min-width: map-get($breakpoints, $breakpoint))
      @content
  @else
    @warn "Unfortunately, no value could be retrieved from `#{$breakpoint}`. Available breakpoints are: #{map-keys($breakpoints)}. "

*
  padding: 0
  margin: 0
  box-sizing: border-box
html,body
  height: 100vh
body
  bottom: 0
  left:  0
  right: 0
  font-family: 'Manrope', sans-serif
  font-weight: 400
ul
  list-style: none
button
  border: none
  background-color: transparent
  cursor: pointer
.container
  margin-left: auto
  margin-right: auto
  max-width: 1020px
  padding-left: 10px
  padding-right: 10px
.row
  margin-left: $gap / 2 * -1px
  margin-right: $gap / 2 * -1px
  margin-bottom: $vstep * 1px
  display: flex
  justify-content: space-between
  flex-wrap: wrap
.col
  width: 100%
  padding-left: $gap / 2 * 1px
  padding-right: $gap / 2 * 1px
  min-height: 100%
@include respond-to('small')
  .col-tablet
    max-width: 100%
    margin-bottom: 16px
@include respond-to('large')
  .col-1-2
    max-width: 100 / 2 * 1%
  .col-1-3
    max-width: 100 / 3 * 1%
.title
  font-weight: bold
  font-size: 32px
  line-height: 32px
  color: #126FB8
  margin-bottom: 30px
</style>
