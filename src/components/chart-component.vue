<template>
  <div class="chart-main-component">
    <div class="chart-component">
      <div class="chart-header">
        <div class="chart-header-balance">
          <p class="chart-header-balance__balance">My balance</p>
          <p class="chart-header-balance__amount-balance">$921.48</p>
        </div>
        <div class="chart-header-icon">
          <img src="../assets/icons/logo.svg" alt="Component logo" />
        </div>
      </div>
      <div class="chart-body">
        <p class="chart-body-header">Spending - Last 7 days</p>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@import '@/assets/colors.scss';
@import '@/assets/fonts.scss';
@media (min-width: 320px) {
  .chart-main-component {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 1em;
    height: 100svh;
    .chart-component {
      display: flex;
      justify-content: space-between;
      flex-direction: column;
      width: 100%;
      .chart-header {
        display: flex;
        justify-content: space-between;
        background-color: $soft-red;
        padding: 1em;
        border-radius: .8em;
        .chart-header-balance {
          &__balance,
          &__amount-balance {
            color: $cream;
            font-size: $primary-size;
            font-weight: $font-weight-size;
          }
          &__amount-balance {
            font-size: $secondary-size;
            font-weight: $font-bold-size;
          }
        }
        .chart-header-icon{
         display: flex;
         align-items: center;
        }
      }
      .chart-body{
        padding: 1em;
        background-color: $very-pale-orange;
        border-radius: .8em;
        .chart-body-header{
          text-align: center;
          font-weight: $font-bold-size;
          font-size: $secondary-size;
        }
      }
    }
  }
}
</style>
<script>
export default {
  name: 'chartComponent',
}
</script>
