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
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              class="inline-block h-6 w-6 stroke-current"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              />
            </svg>
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
          <div class="navbar-center">
            <ul class="top-menu-container menu menu-horizontal uppercase">
              <!-- Navbar menu content here -->
              <li class="ml-3 rounded-full">
                <div
                  class="dropdown dropdown-center dropdown-hover rounded-full"
                >
                  <div tabindex="0" role="button">lịch trực tiếp</div>
                  <DropDownMenuItem />
                </div>
              </li>
              <li class="ml-3 rounded-full">
                <div
                  class="dropdown dropdown-center dropdown-hover rounded-full"
                >
                  <div tabindex="0" role="button">lịch thi đấu</div>
                  <DropDownMenuItem />
                </div>
              </li>
              <li class="ml-3 rounded-full">
                <a class="rounded-full">tỷ lệ kèo</a>
              </li>
              <li class="ml-3 rounded-full">
                <div
                  class="dropdown dropdown-center dropdown-hover rounded-full"
                >
                  <div tabindex="0" role="button">
                    <a>kết quả</a>
                  </div>
                  <DropDownMenuItem />
                </div>
              </li>
              <li class="ml-3 rounded-full">
                <a class="rounded-full">phòng chat</a>
              </li>
              <li class="ml-3 rounded-full">
                <a class="rounded-full">tin tức</a>
              </li>
            </ul>
          </div>
          <div class="navbar-end uppercase">
            <a
              class="btn btn-sm rounded-full mx-1 border-white shadow-xl shadow-black/20"
              >đăng ký</a
            >
            <a class="btn btn-sm rounded-full mx-1 black-gd">
              <span class="text-gold">đăng nhập</span>
            </a>
          </div>
          <!--After User Logged In -->
          <div class="hidden">
            <div class="dropdown dropdown-end">
              <div tabindex="0" role="button" class="btn btn-ghost btn-circle">
                <div class="indicator">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-5 w-5"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"
                    />
                  </svg>
                  <span class="badge badge-sm indicator-item">8</span>
                </div>
              </div>
              <div
                tabindex="0"
                class="card card-compact dropdown-content bg-base-100 z-1 mt-3 w-52 shadow"
              >
                <div class="card-body">
                  <span class="text-lg font-bold">8 Items</span>
                  <span class="text-info">Subtotal: $999</span>
                  <div class="card-actions">
                    <button class="btn btn-primary btn-block">View cart</button>
                  </div>
                </div>
              </div>
            </div>
            <div class="dropdown dropdown-end">
              <div
                tabindex="0"
                role="button"
                class="btn btn-ghost btn-circle avatar"
              >
                <div class="w-10 rounded-full">
                  <img
                    alt="Tailwind CSS Navbar component"
                    src="https://img.daisyui.com/images/stock/photo-1534528741775-53994a69daeb.webp"
                  />
                </div>
              </div>
              <ul
                tabindex="0"
                class="menu menu-sm dropdown-content bg-base-100 rounded-box z-1 mt-3 w-52 p-2 shadow"
              >
                <li>
                  <a class="justify-between">
                    Profile
                    <span class="badge">New</span>
                  </a>
                </li>
                <li><a>Settings</a></li>
                <li><a>Logout</a></li>
              </ul>
            </div>
          </div>
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
  color: #fff;
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
