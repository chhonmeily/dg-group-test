<template>
  <ul
    id="top-up-drop-down"
    tabindex="0"
    class="uppercase dropdown-content menu bg-base-100/50 backdrop-blur rounded-box z-1 w-52 p-2 shadow-sm"
  >
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1">
      <a class="rounded-full"> <span class="menu-icon icon-ball" /> BÓNG ĐÁ</a>
    </li>
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1">
      <a class="rounded-full"> <span class="menu-icon icon-dua-bi" /> Đua bi</a>
    </li>
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1">
      <a class="rounded-full">
        <span class="menu-icon icon-basket-ball" /> BÓNG Rổ</a
      >
    </li>
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1">
      <a class="rounded-full">
        <span class="menu-icon icon-esport" />E-SPORTS</a
      >
    </li>
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1">
      <a class="rounded-full"> <span class="menu-icon icon-casino" />Casino</a>
    </li>
  </ul>
</template>

<style>
.menu-icon {
  display: block;
  width: 30px;
  height: 30px;
  background: url("~/assets/menu-icon.png");
  background-position-y: 0;
  background-size: 100%;
}

.icon-dua-bi {
  background-position-y: -43px;
}

.icon-basket-ball {
  background-position-y: -86px;
}

.icon-esport {
  background-position-y: -129px;
}

.icon-casino {
  background-position-y: -172px;
}
</style>
