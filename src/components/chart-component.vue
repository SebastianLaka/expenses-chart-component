<template>
  <div class="chart-component">
    <div class="chart-header">
      <div class="chart-header-balance">
        <p class="chart-header-balance__balance">My balance</p>
        <p class="chart-header-balance__amount-balance">$921.48</p>
      </div>
    </div>
    <div class="chart-body">
      <p class="chart-body-header">Spending - Last 7 days</p>
    </div>
  </div>
  <p>
    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minus commodi temporibus doloribus
    molestias dignissimos illum, sed perspiciatis ex dolorem obcaecati?
  </p>
</template>
<style lang="scss" scoped>
@import '@/assets/colors.scss';
@import '@/assets/fonts.scss';
.chart-component {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  height: 100svh;
  .chart-header {
    .chart-header-balance {
      background-color: $soft-red;
      &__balance,
      &__amount-balance {
        color: $cream;
        font-size: $primary-size;
      }
      &__amount-balance{
        font-size: $secondary-size;
        font-weight: $font-bold-size;
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
