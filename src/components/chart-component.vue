<template>
  <div class="main-component">
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
      <div class="body-component">
        <p class="body-component__header">Spending - Last 7 days</p>
        <div class="chart-diagrams">
          <div class="mon-chart">
            <div class="mon-chart__chart"></div>
            <p class="mon-chart__day">mon</p>
          </div>
          <div class="tue-chart">
            <div class="tue-chart__chart"></div>
            <p class="tue-chart__day">tue</p>
          </div>
          <div class="wed-chart">
            <div class="wed-chart__chart"></div>
            <p class="wed-chart__day">wed</p>
          </div>
          <div class="thu-chart">
            <div class="thu-chart__chart"></div>
            <p class="thu-chart__day">thu</p>
          </div>
          <div class="fri-chart">
            <div class="fri-chart__chart"></div>
            <p class="fri-chart__day">fri</p>
          </div>
          <div class="sat-chart">
            <div class="sat-chart__chart"></div>
            <p class="sat-chart__day">sat</p>
          </div>
          <div class="sun-chart">
            <div class="sun-chart__chart"></div>
            <p class="sun-chart__day">sun</p>
          </div>
        </div>
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
  .main-component {
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
      .body-component {
        display: flex;
        flex-direction: column;
        padding: 1em;
        background-color: $very-pale-orange;
        border-radius: 0.8em;
        gap: 1em 0;
        &__header {
          text-align: center;
          font-weight: $font-bold-size;
          font-size: $secondary-size;
        }
        .chart-diagrams {
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          .mon-chart, .tue-chart, .wed-chart, .thu-chart, .fri-chart, .sat-chart, .sun-chart{
            &__day{
              color: $medium-brown;
              text-align: center;
            }
            &__chart{
              height: 20px;
              background-color: black;
              width: 2em;
            }
          }
        }
        .chart-body-footer {
          display: flex;
          justify-content: space-between;
          .chart-total,
          .chart-increase {
            &__amount {
              font-size: $secondary-size;
            }
            &__title {
              color: $medium-brown;
            }
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
