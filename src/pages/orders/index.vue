<template>
  <div class="orders">
    <div class="orders__wrapper wrapper">
      <div class="orders__box orders__box--header">
        <div class="orders__counter">
          <h1 class="orders__title">My orders</h1>
          <div class="orders__num">12</div>
        </div>

        <div class="orders__search">
          <input type="search" placeholder="Search Orders by Number" class="orders__input">
        </div>
      </div>

      <OrderFilter></OrderFilter>

      <div class="orders__list">
        <OrderPreview step="1"></OrderPreview>
        <OrderPreview step="5"></OrderPreview>
        <OrderPreview step="3"></OrderPreview>
        <OrderPreview step="2"></OrderPreview>
      </div>

      <BasePagination></BasePagination>

    
    </div>
  </div>
</template>

<script>
  import OrderFilter from '@/components/order/filter/OrderFilter.vue'
  import OrderPreview from '@/components/order/OrderPreview.vue'
  import BasePagination from '@/components/base/BasePagination.vue'

  export default {
    name: 'Orders',
    components: {
      OrderFilter,
      OrderPreview,
      BasePagination
    }
  }

</script>

<style lang="scss">
  .orders {
    padding-top: 86px;
  }

  .orders__box--header {
    display: flex;
    align-items: center;
    padding-bottom: 48px;
  }

  .orders__counter {
    display: flex;
    align-items: flex-end;
  }

  .orders__title {
    font-size: 34px;
    line-height: 41px;
    font-weight: 600;
    color: #000000;
    white-space: nowrap;
  }

  .orders__num {
    position: relative;
    top: -7px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-left: 8px;
    margin-right: 32px;
    padding: 1px 9px;
    background: #FFFFFF;
    border-radius: 30px;
    font-size: 15px;
    font-weight: 400;
  }

  .orders__search {
    width: 100%;
    max-width: 405px;
  }

  .orders__input {
    width: 100%;
    padding: 11px 11px 11px 44px;
    height: 40px;
    box-sizing: border-box;
    font-size: 13px;
    font-weight: 500;
    background: #E6E9EE;
    border-radius: 6px;
    
  }

</style>
