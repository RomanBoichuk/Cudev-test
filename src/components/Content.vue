<template>
  <div class="section1">
    <div class="container">
      <div class="row">
        <div class="col col-1-2 col-tablet">
          <p class="section1__title">Enter your vehicle details to receive a free valuation</p>
          <p class="section1__description">
              If your vehicle has <b>less than 100,000 milesl</b> enter your vehicle and
              contact details and we will contact you with a cash valuation
              within 24 hours.
          </p>
        </div>
        <div class="col col-1-2 col-tablet">
          <div class="col_inner">
            <button class="section1__btn">ENTER REG</button>
            <div class="inputcheck">
              <label>
                <input type="checkbox" id="vehicle " name="vehicle">
                  <p>
                    I confirm that the vehicle I am enquiring about has less than 100,000 miles.
                  </p>
              </label>
            </div>
            <button class="btn">Get Started <span class="btn_icon"><font-awesome-icon icon="arrow-alt-circle-right"/></span></button>
          </div>
        </div>
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
.section1
  max-width: 1440px
  margin-left: auto
  margin-right: auto
  background: linear-gradient(79.95deg, rgba(18, 111, 184, 0.2) 2.62%, rgba(18, 111, 184, 0) 98.24%)
  padding: 182px 0 188px 0
.section1__title
  font-weight: 800
  font-size: 48px
  line-height: 60px
  color: #126FB8
  margin-bottom: 26px
.section1__description
  font-style: normal
  font-weight: normal
  font-size: 24px
  line-height: 36px
  color: #252851
.section1__btn
  font-family: 'UKNumberPlate', sans-serif
  font-size: 48px
  line-height: 48px
  color: #126FB8
  text-align: center
  background: #FFFFFF
  box-shadow: 0px 4px 8px rgba(37, 40, 81, 0.1)
  border-radius: 8px
  padding: 9px 90px
  margin-bottom: 26px
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
.col_inner
  display: flex
  flex-direction: column
  max-width: 407px
  padding-top: 18%
.inputcheck
  margin-bottom: 26px
label
  display: flex
input
  width: 26px
  height: 26px
  background: #FFFFFF
  box-shadow: 0px 4px 8px rgba(37, 40, 81, 0.1)
  border-radius: 2px
  margin-right: 16px
p
  font-size: 16px
  line-height: 24px
@media (max-width: 376px)
  .section1
    padding: 98px 14px 111px 14px
  .section1__title
    font-size: 36px
    line-height: 45px
    margin-bottom: 16px
  .section1__description
    font-size: 16px
    line-height: 24px
  .col_inner
    padding-top: 42px
  .section1__btn
    font-size: 36px
    line-height: 36px
    padding: 9px 50px
  .btn
    padding: 15px 94px 15px 92px
</style>
