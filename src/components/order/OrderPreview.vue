<template>
  <div class="order-preview">
    <div class="order-preview__content">
      <div class="order-preview__details preview-details">
        <div class="preview-details__box">

          <p class="preview-details__num">44367 — 23 — 21</p>
          <p class="preview-details__title">Order Number</p>

          <div class="preview-details__list">
            <div class="preview-details__item">
              <p class="preview-details__data">Palette</p>
              <p class="preview-details__title">Type</p>
            </div>

            <div class="preview-details__item">
              <p class="preview-details__data">80x120</p>
              <p class="preview-details__title">Format</p>
            </div>

            <div class="preview-details__item">
              <p class="preview-details__data">180 CM</p>
              <p class="preview-details__title">Height</p>
            </div>

            <div class="preview-details__item">
              <p class="preview-details__data">55</p>
              <p class="preview-details__title">Amount</p>
            </div>

            <div class="preview-details__item">
              <p class="preview-details__data">49 kg</p>
              <p class="preview-details__title">Weight</p>
            </div>
          </div>
        </div>

        <div class="preview-details__box preview-details__box--price">
          <div class="review-details__price">
            <p class="preview-details__data preview-details__data--price">€ 5 100.00</p>
            <p class="preview-details__title">Price</p>
          </div>

          <button class="preview-details__button">Comment price</button>

        </div>

      </div>

      <div class="order-preview__status preview-status">
        <div class="preview-status__box preview-status__box--progress">
          <p class="preview-status__status">In progress</p>
          <div class="preview-status__buttons">
            <button class="preview-status__button preview-status__button--copy">Copy</button>
            <button class="preview-status__button preview-status__button--cancel">Cancel</button>
          </div>
        </div>

        <div class="preview-status__loading loading">
          <div class="loading__item"
               :class="getClass(1, step)">
            <div class="loading__line"></div>
          </div>
          <div class="loading__item"
               :class="getClass(2, step)">
            <div class="loading__line"></div>
          </div>
          <div class="loading__item"
               :class="getClass(3, step)">
            <div class="loading__line"></div>
          </div>
          <div class="loading__item"
               :class="getClass(4, step)">
            <div class="loading__line"></div>
          </div>
          <div class="loading__item"
               :class="getClass(5, step)">
            <div class="loading__line"></div>
          </div>
        </div>

        <div class="preview-status__list">
          <div class="preview-status__item">
            <p class="preview-status__title">Loading: 07/04/2020 15:30</p>
            <p class="preview-status__data">200 Quai de Valmy, 75010 Paris</p>
          </div>

          <div class="preview-status_item">
            <p class="preview-status__title">Delivery: 15/04/2020 18:00</p>
            <p class="preview-status__data">1 Route de Saint-Saulgé, 58800 Corbigny</p>
          </div>
        </div>

        <p class="preview-status__title">Additional information</p>
        <div class="preview-status__box">
          <p class="preview-status__text">The slip includes, in particular, the description of the goods to be transported, th The slip includes, in particular, the description of the goods to be transported, th</p>
          <button class="preview-status__more">Read more</button>
        </div>
      </div>
    </div>
    
  </div>
</template>

<script>
  // import BaseCheckbox from '@/components/base/BaseCheckbox.vue'

  export default {
    name: 'OrderFilter',
    components: {
      // BaseCheckbox
    },
    props: {
      step: {type: Number},
    },
    methods:{
      getClass(a, step){
        if (a > step)
          return false;
        if (a < step)
          return 'active';
        else
          return 'current';
      }
    }
  }
</script>

<style lang="scss">
  .order-preview__content {
    display: flex;
    flex-direction: column;
    position: relative;
    margin-bottom: 28px;

    &:before {
      content: "";
      position: absolute;
      bottom: -8px;
      left: 15px;
      right: 15px;
      height: 18px;
      background: #FFFFFF;
      box-shadow: 0px 27px 64px rgba(167, 185, 226, 0.1);
      border-radius: 8px;
      z-index: 0;
    }

    @media (min-width: $viewport-tablet) {
      flex-direction: row;
    }
  }

  .order-preview__details {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 100%;
    
    padding: 26px 10px;
    flex: 1;
    background: #1C2377;
    box-shadow: 0px 7px 64px rgba(0, 0, 0, 0.04);
    border-radius: 8px 0 0 8px;
    box-sizing: border-box;
    z-index: 2;

    @media (min-width: $viewport-tablet) {
      padding: 26px;
      max-width: 506px;
    }
  }

  .order-preview__status {
    padding: 26px 10px;
    flex: 1;
    background: #FFFFFF;
    box-shadow: 0px 27px 64px rgba(167, 185, 226, 0.1);
    border-radius: 0 8px 8px 0;
    box-sizing: border-box;
    z-index: 2;

    @media (min-width: $viewport-tablet) {
      padding: 26px;
    }
  }

  .preview-details__num {
    margin-bottom: 9px;
    font-weight: 500;
    font-size: 32px;
    line-height: 28px;
    color: #10ACFF;
  }

  .preview-details__title {
    font-weight: 400;
    font-size: 10px;
    line-height: 16px;
    color: #A7B9E2;

    @media (min-width: $viewport-tablet) {
      font-size: 12px;
    }
  }

  .preview-details__list {
    margin: 32px -5px 30px -5px;
    display: flex;
    justify-content: space-between;
  }

  .preview-details__item {
    margin: 0 5px;

  }

  .preview-details__data {
    margin-bottom: 8px;
    font-weight: 500;
    font-size: 10px;
    line-height: 13px;
    color: #FFFFFF;

    @media (min-width: $viewport-tablet) {
      font-size: 12px;
    }
  } 

  .preview-details__data--price {
    font-size: 16px;

    @media (min-width: $viewport-tablet) {
      font-size: 22px;
    }
  }

  .preview-details__box--price {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .preview-details__button {
    padding: 8px 13px;
    font-size: 12px;
    background: #3766D5;
    color: #FFFFFF;

    @media (min-width: $viewport-tablet) {
      padding: 10px 17px;
      font-size: 14px;
    }
    
    &:hover {
      background: #2750b1;
    }
  }

  .preview-status__box {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .preview-status__box--progress {
    margin-bottom: 38px;
  }

  .preview-status__status {
    position: relative;
    padding-left: 23px;
    font-weight: 500;
    font-size: 12px;
    line-height: 23px;
    text-transform: uppercase;

    @media (min-width: $viewport-tablet) {
      font-size: 16px;
    }

    &:before {
      content: "";
      position: absolute;
      top: calc(50% - 8px);
      left: 0;
      height: 15px;
      width: 15px;
      background: #008BD5;
      border-radius: 2px;
    }
  }

  .preview-status__buttons {
    display: flex;
  }

  .preview-status__button {
    margin-left: 10px;
    position: relative;
    padding: 5px 8px 5px 30px;
    background: #f5f6f9;
    border-radius: 44px;
    box-sizing: border-box;
    font-size: 13px;
    line-height: 20px;
    font-weight: 400;

    @media (min-width: $viewport-tablet) {
      padding: 5px 22px 5px 35px;
    }

    &:before {
      content: "";
      position: absolute;
      left: 11px;
      top: 50%;
      transform: translateY(-50%);
      width: 14px;
      height: 14px;
      background-size: cover;
      background-repeat: no-repeat;
    }

    &:hover {
      background: #dbdbdd;
    }
  }

  .preview-status__button--copy {
    &:before {
      background-image: url("~@/assets/images/copy.svg");
    }
  }

  .preview-status__button--cancel {
    &:before {
      background-image: url("~@/assets/images/cancel.svg");
    }
  }

  .loading {
    display: flex;
    align-items: flex-end;
    height: 20px;
    margin: 0 -1px 16px -1px;
  }

  .loading__item {
    width: 20%;
    height: 6px;
    position: relative;

    &:first-child {
      .loading__line {
        border-radius: 3px 0 0 3px;
      }
    }

    &:last-child {
      .loading__line {
        border-radius: 0 3px 3px 0;
      }
    }

    &.active {
      .loading__line {
        background: #008BD5;
      }
    }

    &.current {
      .loading__line {
        background: #008BD5;
      }

      &:before {
        content: "";
        position: absolute;
        width: 31px;
        height: 17px;
        top: -20px;
        right: 10px;
        background-image: url("~@/assets/images/loading-car.svg");
        background-size: cover;
        background-repeat: no-repeat;
      }
    }
  }

  .loading__line {
    width: calc(100% - 2px);
    height: 100%;
    background: #F1F4FA;
    margin: 0 1px;    
  }

  .preview-status__list {
    display: flex;
    margin: 0 -10px 31px -10px;
  }

  .preview-status__item {
    width: 50%;
    margin: 0 10px;
  }

  .preview-status__title {
    margin-bottom: 8px;
    font-weight: 400;
    font-size: 10px;
    line-height: 16px;
    color: #A7B9E2;

    @media (min-width: $viewport-tablet) {
      font-size: 14px;
    }
  }

  .preview-status__data {
    font-weight: 500;
    font-size: 10px;
    line-height: 20px;

    @media (min-width: $viewport-tablet) {
      font-size: 14px;
    }
  }

  .preview-status__text {
    font-size: 14px;
    line-height: 20px;
    font-weight: 400;
    padding-right: 5px;
    display: -webkit-box;
    -webkit-line-clamp: 1;
    -webkit-box-orient: vertical;
    overflow: hidden;
    text-overflow: ellipsis;
  }

  .preview-status__more {
    position: relative;
    padding-right: 12px;
    white-space: nowrap;
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
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
