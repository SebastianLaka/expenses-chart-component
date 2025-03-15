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
        <p class="chart-body__header">Spending - Last 7 days</p>
        <div class="body-diagrams"></div>
        <div class="chart-body-footer">
          <div class="chart-total">
            <p class="chart-total__title">Total this month</p>
            <p class="chart-total__amount">$478.33</p>
          </div>
          <div class="chart-increase">
            <p class="chart-increase__amount">+2.4%</p>
            <p class="chart-increase__title">from last month</p>
          </div>
        </div>
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
      gap: 1em 0;
      .chart-header {
        display: flex;
        justify-content: space-between;
        background-color: $soft-red;
        padding: 1em;
        border-radius: 0.8em;
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
        .chart-header-icon {
          display: flex;
          align-items: center;
        }
      }
      .chart-body {
        display: flex;
        flex-direction: column;
        padding: 1em;
        background-color: $very-pale-orange;
        border-radius: 0.8em;
        &__header {
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
