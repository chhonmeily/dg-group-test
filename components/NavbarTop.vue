<script setup>
import BurgerIcon from "~/assets/burger-menu.svg";
</script>
<template>
  <div class="w-full bg-gold">
    <div class="@container">
      <div class="max-w-7xl mx-auto">
        <div class="flex align-items xl:hidden">
          <label
            for="my-drawer-3"
            aria-label="open sidebar"
            class="btn btn-square btn-ghost m-3"
          >
            <BurgerIcon />
          </label>

          <div
            class="text-[48px] mt-[-5px] uppercase inline-block xl:hidden text-center"
          >
            <a href="/">Logo</a>
          </div>
        </div>

        <!-- Navbar -->
        <div class="navbar w-full hidden xl:flex">
          <div class="navbar-start" />
          <div class="navbar-center pt-4 ml-[-60px]">
            <ul class="top-menu-container menu menu-horizontal uppercase">
              <!-- Navbar menu content here -->
              <li class="rounded-full">
                <div
                  class="dropdown dropdown-center dropdown-hover rounded-full"
                >
                  <div tabindex="0" role="button">lịch trực tiếp</div>
                  <DropDownMenuItem />
                </div>
              </li>
              <li class="rounded-full">
                <div
                  class="dropdown dropdown-center dropdown-hover rounded-full"
                >
                  <div tabindex="0" role="button">lịch thi đấu</div>
                  <DropDownMenuItem />
                </div>
              </li>
              <li class="rounded-full">
                <a class="rounded-full">tỷ lệ kèo</a>
              </li>
              <li class="rounded-full">
                <div
                  class="dropdown dropdown-center dropdown-hover rounded-full"
                >
                  <div tabindex="0" role="button">
                    <a>kết quả</a>
                  </div>
                  <DropDownMenuItem />
                </div>
              </li>
              <li class="rounded-full">
                <a class="rounded-full">phòng chat</a>
              </li>
              <li class="rounded-full">
                <a class="rounded-full">tin tức</a>
              </li>
            </ul>
          </div>
          <div class="navbar-end uppercase flex pt-3">
            <a
              class="btn btn-sm rounded-full mx-1 border-white shadow-xl shadow-black/20"
              >đăng ký</a
            >
            <a class="btn btn-sm rounded-full mx-1 black-gd">
              <span class="text-gold">đăng nhập</span>
            </a>
          </div>
          <!--After User Logged In -->
          <LoginMenuSection />
        </div>
        <!--End Of Navbar-->
      </div>
      <!--End OF Navbar Container-->
    </div>
  </div>
</template>
<style>
.top-menu-container li,
.top-menu-container .dropdown li {
  color: #000000;
  border: 1px solid transparent;
}

.top-menu-container li:hover,
.top-menu-container li:active,
.top-menu-container li:focus {
  background: linear-gradient(180deg, #5c5c5c 0%, #000000 100%);
  border: 1px solid var(--Color-3, rgba(26, 26, 26, 1));
  box-shadow: 0px 5px 11px 0px var(--BlackalphaBlack10);
  box-shadow: 0px 20px 20px 0px var(--BlackalphaBlack9);
  box-shadow: 0px 45px 27px 0px var(--BlackalphaBlack5);
  box-shadow: 0px 79px 32px 0px var(--Color-sdsdColor-sd11);
}

.top-menu-container li:hover,
.top-menu-container li:hover > a,
.top-menu-container li:active,
.top-menu-container li:active > a,
.top-menu-container li:focus,
.top-menu-container li:focus > a {
  color: #000;
}

.top-menu-container li a:focus,
.top-menu-container li a:active,
.top-menu-container li a:hover,
.top-menu-container .dropdown:hover,
.top-menu-container .dropdown:active,
.top-menu-container .dropdown:focus,
.top-menu-container .dropdown:focus-within {
  background: linear-gradient(to right, #f8e889, #e4b764);
  background-clip: text;
  color: transparent;
}
</style>
