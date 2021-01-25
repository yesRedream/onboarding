<template>
  <div class="header">
    <div class="header__wrapper wrapper">
      <div class="header__content">
        <a href="#" class="header__box header__box--logo">
          <img src="./../../assets/images/logo.svg" alt="" class="header__logo">
        </a>

        <div class="header__list">
          <a href="#" class="header__item">Orders</a>
        </div>

        <a href="#" class="header__profile header-profile">
          <p class="header-profile__name">Spiche Technologies</p>
          <div class="header-profile__box">
            <img src="./../../assets/images/profile.svg" alt="" class="header-profile__img">

          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>

</script>

<style lang="scss">
  .header {
    background: #1C2377;
  }

  .header__wrapper {}

  .header__content {
    height: 60px;
    box-sizing: border-box;
    display: flex;
    align-items: center;
  }

  .header__box--logo {
    margin-right: 30px;
    width: 120px;

    @media (min-width: $viewport-tablet) {
      margin-right: 75px;
      width: 200px;
    }
  }

  .header__logo {
    width: 100%;
  }

  .header__list {
    display: flex;
    height: 100%;
  }

  .header__item {
    display: flex;
    align-items: center;
    height: 100%;
    padding: 0 30px;
    font-size: 13px;
    font-weight: 500;
    color: #FFFFFF;
    border-bottom: 4px solid #FF4048;
    box-sizing: border-box;

    &:hover {
      background: #161c5a;
    }
  }

  .header-profile {
    margin-left: auto;
    display: flex;
    align-items: center;
    height: 100%;
    padding: 0 2px 0 15px;

    &:hover {
      background: #161c5a;
    }
  }

  .header-profile__box {
    width: 36px;
    height: 36px;
  }

  .header-profile__img {
    width: 100%;
  }

  .header-profile__name {
    display: none;
    

    @media (min-width: $viewport-mobile) {
      display: block;
      margin-right: 12px;
      font-size: 13px;
      font-weight: 500;
      color: #FFFFFF;
    }
  }

</style>
