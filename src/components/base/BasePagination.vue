<template>
  <div class="pagination">
    <div class="pagination__list">
      <a href="" class="pagination__item active">
        <span class="pagination__text">1</span>
      </a>
      <a href="" class="pagination__item">
        <span class="pagination__text">2</span>
      </a>
      <a href="" class="pagination__item">
        <span class="pagination__text">3</span>
      </a>
      <div class="pagination__item disabled">
        <span class="pagination__text">...</span>
      </div>
      <a href="" class="pagination__item">
        <span class="pagination__text">27</span>
      </a>
    </div>
  </div>
</template>

<script>

</script>

<style lang="scss">
  .pagination {
    padding-bottom: 100px;
  }

  .pagination__list {
    display: flex;
  }

  .pagination__item {
    width: 100%;
    max-width: 78px;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
    box-sizing: border-box;
    background: #FFFFFF;
    border: 1px solid #EBEBEB;
    border-left: none;

    &.active {
      background: #1C2377;
      border: none;

      .pagination__text {
        color: #FFFFFF;
      }
    }

    &.disabled {
      background: transparent;
    }
  }

  .pagination__text {
    font-size: 12px;
    font-weight: 700;
    line-height: 14px;
    color: #000000
  }


</style>
