<template>
  <label class="checkbox">
    <slot/>
    <span class="checkbox__data"
          :class="color">
      <span class="checkbox__text">{{ text }}</span>
    </span>
  </label>
</template>

<script>
  export default {
    name: 'BaseCheckbox',
    props: {
      text: {type: String},
      color: {type: String},
    }
  }
</script>

<style lang="scss">
  .checkbox {
    position: relative;
    cursor: pointer;
    height: 30px;
    box-sizing: border-box;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  input {
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 0;
    clip: rect(0,0,0,0);

    &:checked ~ .checkbox__data {
      padding: 3px 15px;
      background: #FFFFFF;
      box-shadow: 0px 0px 9px rgba(0, 55, 184, 0.2);

      &.blue,
      &.red,
      &.green,
      &.light {
        padding-left: 20px;

        &:before {
          left: 10px;
        }
      }

      .checkbox__text {
        font-size: 13px;
        text-transform: none;
        color: #3766D5;
      }
    }
  }

  .checkbox__data {
    display: flex;
    align-items: center;
    padding: 3px 0 3px 15px;
    margin: 0 10px 0 5px;
    border-radius: 36px;
    height: 30px;
    box-sizing: border-box;
    height: 100%;

    &.blue,
    &.red,
    &.green,
    &.light {
      position: relative;

      &:before {
        content: "";
        display: block;
        width: 6px;
        height: 6px;
        border-radius: 100%;
        position: absolute;
        left: 5px;
        top: calc(50% - 2px);
      }
    }

    &.blue {
      &:before {
        background: #008BD5;
      }
    }

    &.red {
      &:before {
        background: #FF4048;
      }
    }

    &.green {
      &:before {
        background: #2ED47A;
      }
    }

    &.light {
      &:before {
        background: #A7B9E2;
      }
    }
  }


  .checkbox__text {
    font-weight: 500;
    font-size: 10px;
    font-weight: 700;
    line-height: 13px;
    text-transform: uppercase;
  }
</style>
