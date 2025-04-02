<template>
  <div class="main-component">
    <div class="chart-component">
      <div class="chart-header">
        <div class="chart-header-balance">
          <p class="chart-header-balance__balance">My balance</p>
          <p class="chart-header-balance__amount-balance">$921.48</p>
        </div>
        <div class="chart-header-icon-container">
          <img src="../assets/icons/logo.svg" alt="Component logo" class="logo" />
        </div>
      </div>
      <div class="body-component">
        <p class="body-component__header">Spending - Last 7 days</p>
        <div class="chart-diagrams">
          <div class="mon-chart" v-for="(chartItem, index) in data" :key="index">
            <p class="mon-chart__day">{{ chartItem.day }}</p>
            <div class="mon-chart__chart" :style="{ height: chartItem.amount * 2.5 + 'px' }"></div>
            <p class="mon-chart__chart-value">%{{ chartItem.amount }}</p>
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
@media (min-width: 375px) {
    .main-component {
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100svh;
      padding: 0.4em;
      .chart-component {
        display: flex;
        justify-content: space-between;
        flex-direction: column;
        flex-wrap: wrap;
        min-width: 100%;
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
              font-size: $mobile-font-size;
              font-weight: $font-weight-size;
            }
            &__amount-balance {
              font-size: $primary-size;
              font-weight: $font-bold-size;
            }
          }
          .chart-header-icon-container {
            display: flex;
            align-items: center;
          }
        }
        .body-component {
          display: flex;
          flex-direction: column;
          background-color: $very-pale-orange;
          border-radius: 0.8em;
          gap: 2em;
          margin-top: 0.5em;
          &__header {
            text-align: center;
            font-weight: $font-bold-size;
            font-size: $primary-size;
          }
          .chart-diagrams {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            .mon-chart {
              display: flex;
              flex-direction: column-reverse;
              align-items: center;
              &__day {
                color: $medium-brown;
              }
              &__chart {
                background-color: $soft-red;
                width: 2em;
                border-radius: 0.4em;
              }
              &__chart-value {
                color: $very-pale-orange;
                background-color: $dark-brown;
                padding: 0.3em;
                margin-bottom: 0.5em;
                border-radius: 0.4em;
                font-family: inherit;
                font-size: $mobile-font-size;
              }
            }
          }
          .chart-body-footer {
            display: flex;
            justify-content: space-between;
            .chart-total,
            .chart-increase {
              &__amount {
                font-size: $primary-size;
              }
              &__title {
                color: $medium-brown;
                font-size: $mobile-font-size;
              }
            }
          }
        }
      }
    }
  }

@media (min-width: 475px) {
  .main-component {
    .chart-component {
      .chart-header{
        .chart-header-balance{
          &__balance{
            font-size: $primary-size;
          }
          &__amount-balance{
            font-size: $secondary-size;
          }
        }
      }
      .body-component {
        padding: 1.5em;
        &__header{
          font-size: $secondary-size;
        }
        .chart-diagrams {
          .mon-chart {
            &__chart {
              min-width: 2.5em;
            }
          }
        }
        .chart-body-footer {
            .chart-total,
            .chart-increase {
              &__amount {
                font-size: $secondary-size;
              }
              &__title {
                color: $medium-brown;
                font-size: $primary-size;
              }
            }
          }
      }
    }
  }
}
</style>
<script>
import dataJson from '@/assets/data.json'
export default {
  name: 'chartComponent',
  data() {
    return {
      data: dataJson,
    }
  },
}
</script>
