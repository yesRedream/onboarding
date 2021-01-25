<template>
  <div class="filter">
    <div class="filter__content">
      <div class="filter__box filter__box--checkbox">
        <p class="filter__title">Show:</p>

        <BaseCheckbox text="All Types" class="filter__checkbox">
          <input
            type="checkbox"
            class="filter__checkbox-input"
            name="filter"
          >
        </BaseCheckbox>

        <BaseCheckbox text="New" color="blue" class="filter__checkbox">
          <input
            type="checkbox"
            class="filter__checkbox-input"
            name="filter"
          >
        </BaseCheckbox>

        <BaseCheckbox text="In progress" color="blue" class="filter__checkbox">
          <input
            type="checkbox"
            class="filter__checkbox-input"
            name="filter"
          >
        </BaseCheckbox>

        <BaseCheckbox text="Proposition sent" color="blue" class="filter__checkbox">
          <input
            type="checkbox"
            class="filter__checkbox-input"
            name="filter"
          >
        </BaseCheckbox>

        <BaseCheckbox text="Confirmed" color="blue" class="filter__checkbox">
          <input
            type="checkbox"
            class="filter__checkbox-input"
            name="filter"
          >
        </BaseCheckbox>

        <BaseCheckbox text="Completed" color="green" class="filter__checkbox">
          <input
            type="checkbox"
            class="filter__checkbox-input"
            name="filter"
          >
        </BaseCheckbox>

        <BaseCheckbox text="Canceled" color="light" class="filter__checkbox">
          <input
            type="checkbox"
            class="filter__checkbox-input"
            name="filter"
          >
        </BaseCheckbox>

        <BaseCheckbox text="Rejected" color="red" class="filter__checkbox">
          <input
            type="checkbox"
            class="filter__checkbox-input"
            name="filter"
          >
        </BaseCheckbox>

        

      </div>

      <div class="filter__box filter__box--dropdown">
        <p class="filter__title">Loading Date:</p>
        <button class="filter__toggle">This week</button>

      </div>

    </div>
    
  </div>
</template>

<script>
  import BaseCheckbox from '@/components/base/BaseCheckbox.vue'

  export default {
    name: 'OrderFilter',
    components: {
      BaseCheckbox
    }
  }

</script>

<style lang="scss">
  .filter__content {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-bottom: 10px;
  }
  .filter__box--checkbox {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
  }

  .filter__box--dropdown {
    display: flex;
    align-items: center;    
  }

  .filter__title {
    margin-right: 10px;
    margin-bottom: 10px;
    font-size: 13px;
    font-weight: 300;
  }

  .filter__checkbox {
    margin-bottom: 10px;
    box-sizing: border-box;
  }

  .filter__toggle {
    position: relative;
    margin-bottom: 10px;
    padding-right: 12px;
    white-space: nowrap;
    font-weight: 700;
    font-size: 13px;
    line-height: 18px;
    color: #3766D5;

    &:hover {
      color: #008BD5;
    }

    &:before {
      content: "";
      position: absolute;
      right: 0;
      top: 50%;
      transform: translateY(-50%);
      width: 6px;
      height: 4px;
      background-image: url("~@/assets/images/arrow-down.svg");
      background-size: cover;
      background-repeat: no-repeat;
    }
  }

</style>
