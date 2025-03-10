<template>
  <div class="chart-component">
    <div class="chart-header">
      <p class="chart-header__balance">My balance</p>
      <p class="chart-header__amount-balance">$921.48</p>
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
.chart-component {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  height: 100svh;
  .chart-header {
    background-color: $soft-red;
    &__balance,
    &__amount-balance {
      color: $cream;
    }

  }
}
</style>
<script>
export default {
  name: 'chartComponent',
}
</script>
