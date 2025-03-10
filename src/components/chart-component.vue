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
    justify-content: center;
    align-items: center;
    .chart-component {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      height: 100svh;
      width: 75%;
      .chart-header {
        display: flex;
        background-color: $soft-red;
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
