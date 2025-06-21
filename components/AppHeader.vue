<template>
  <header>
    <div class="drawer">
      <!-- eslint-disable-next-line vue/html-self-closing -->
      <input id="my-drawer-3" type="checkbox" class="drawer-toggle hidden" />
      <div class="drawer-content flex flex-col relative">
        <div
          class="hidden xl:block w-[25%] h-[107px] absolute top-0 left-0 rounded-r-full bg-black text-right text-white pr-[20px]"
        >
          <h1 class="text-[76px] mt-[-5px] uppercase">
            <a href="/">Logo</a>
          </h1>
        </div>
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
                  <ul class="menu menu-horizontal uppercase">
                    <!-- Navbar menu content here -->
                    <li class="pl-3"><a>lịch trực tiếp</a></li>
                    <li class="pl-3"><a>lịch thi đấu</a></li>
                    <li class="pl-3"><a>tỷ lệ kèo</a></li>
                    <li class="pl-3"><a>kết quả</a></li>
                    <li class="pl-3"><a>phòng chat</a></li>
                    <li class="pl-3"><a>tin tức</a></li>
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
                    <div
                      tabindex="0"
                      role="button"
                      class="btn btn-ghost btn-circle"
                    >
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
                          <button class="btn btn-primary btn-block">
                            View cart
                          </button>
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
        <div class="w-full bg-black">
          <div class="@container">
            <div class="max-w-7xl mx-auto">
              <!-- Navbar -->
              <div class="navbar hidden xl:flex">
                <div class="navbar-start" />
                <div class="navbar-center flex-none">
                  <ul class="menu menu-horizontal">
                    <!-- Navbar menu content here -->
                    <li class="px-4 text-gold"><a>Bảng Tin</a></li>
                    <li class="px-4 text-gold"><a>Reels</a></li>
                    <li class="px-4 text-gold"><a>Highlight</a></li>
                    <li class="px-4 text-gold"><a>Tip Kèo</a></li>
                    <li class="px-4 text-gold"><a>Phim Ảnh</a></li>
                    <li class="px-4 text-gold"><a>Truyện Tranh</a></li>
                  </ul>
                </div>
                <div class="navbar-end">
                  <a class="btn btn-sm rounded-full uppercase mx-2">
                    <svg
                      class="px-0"
                      width="30"
                      height="31"
                      viewBox="0 0 30 31"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <g clip-path="url(#clip0_18867_599)">
                        <path
                          d="M15 29.5C22.732 29.5 29 23.232 29 15.5C29 7.76801 22.732 1.5 15 1.5C7.26802 1.5 1 7.76801 1 15.5C1 23.232 7.26802 29.5 15 29.5Z"
                          fill="#FF1D1D"
                        />
                        <path
                          d="M15 8.8042L16.511 13.4542H21.4003L17.4447 16.3281L18.9556 20.9781L15 18.1043L11.0445 20.9781L12.5554 16.3281L8.59985 13.4542H13.4891L15 8.8042Z"
                          fill="#F8E889"
                        />
                        <path
                          opacity="0.25"
                          d="M23.8799 6.34092C25.9228 9.89006 21.7471 13.8787 16.3863 16.9645C11.0254 20.0504 4.56429 21.5224 3.39668 18.2779C2.00997 14.4248 3.79246 7.73122 9.15337 4.64537C14.5142 1.55952 21.8369 2.79181 23.8799 6.34092Z"
                          fill="white"
                        />
                      </g>
                      <defs>
                        <clipPath id="clip0_18867_599">
                          <rect
                            width="28"
                            height="28"
                            fill="white"
                            transform="translate(1 1.5)"
                          />
                        </clipPath>
                      </defs>
                    </svg>
                    <span class="px-0"> tiếng việt </span>
                  </a>
                  <div>
                    <label class="toggle w-[60px] text-base-content">
                      <input type="checkbox" />
                      <!-- <svg
                        aria-label="enabled"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 24 24"
                      >
                        <g
                          stroke-linejoin="round"
                          stroke-linecap="round"
                          stroke-width="4"
                          fill="none"
                          stroke="currentColor"
                        >
                          <path d="M20 6 9 17l-5-5"></path>
                        </g>
                      </svg> -->
                      <svg
                        aria-label="enabled"
                        width="30"
                        height="31"
                        viewBox="0 0 30 31"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <g clip-path="url(#clip0_18867_753)">
                          <path
                            d="M7.81875 9.42345C8.12422 9.72892 8.61875 9.72892 8.92341 9.42345C9.2281 9.11797 9.2281 8.62345 8.92341 8.31879L7.26642 6.66095C6.96095 6.35547 6.46642 6.35547 6.16172 6.66095C5.85625 6.96642 5.85625 7.46095 6.16172 7.76565L7.81875 9.42345ZM8.28905 21.1172L6.64763 22.7586C6.3453 23.0609 6.3453 23.5508 6.64763 23.8531C6.94996 24.1555 7.43983 24.1555 7.74216 23.8531L9.38358 22.2117C9.68591 21.9094 9.68591 21.4195 9.38358 21.1172C9.08125 20.8149 8.59142 20.8148 8.28905 21.1172ZM15 6.90625C15.4312 6.90625 15.7812 6.55625 15.7812 6.125V3.78125C15.7812 3.35 15.4312 3 15 3C14.5687 3 14.2188 3.35 14.2188 3.78125V6.125C14.2188 6.55625 14.5687 6.90625 15 6.90625ZM22.5164 9.0781L24.1578 7.43668C24.4602 7.13436 24.4602 6.64449 24.1578 6.34216C23.8555 6.03983 23.3656 6.03983 23.0633 6.34216L21.4219 7.98358C21.1195 8.28591 21.1195 8.77578 21.4219 9.0781C21.7242 9.38047 22.2141 9.38047 22.5164 9.0781ZM5.625 14.7188H3.28125C2.85 14.7188 2.5 15.0687 2.5 15.5C2.5 15.9312 2.85 16.2812 3.28125 16.2812H5.625C6.05625 16.2812 6.40625 15.9312 6.40625 15.5C6.40625 15.0687 6.05625 14.7188 5.625 14.7188ZM15 24.0938C14.5687 24.0938 14.2188 24.4438 14.2188 24.875V27.2188C14.2188 27.65 14.5687 28 15 28C15.4312 28 15.7812 27.65 15.7812 27.2188V24.875C15.7812 24.4438 15.4312 24.0938 15 24.0938ZM26.7188 14.7188H24.375C23.9438 14.7188 23.5938 15.0687 23.5938 15.5C23.5938 15.9312 23.9438 16.2812 24.375 16.2812H26.7188C27.15 16.2812 27.5 15.9312 27.5 15.5C27.5 15.0687 27.15 14.7188 26.7188 14.7188ZM22.1812 21.5766C21.8758 21.2711 21.3813 21.2711 21.0766 21.5766C20.7711 21.8821 20.7711 22.3766 21.0766 22.6812L22.7336 24.3383C23.0391 24.6438 23.5336 24.6438 23.8383 24.3383C24.143 24.0328 24.1438 23.5383 23.8383 23.2336L22.1812 21.5766ZM15 8.46405C11.1141 8.46405 7.96405 11.6141 7.96405 15.5C7.96405 19.3859 11.1141 22.5359 15 22.5359C18.8859 22.5359 22.0359 19.3859 22.0359 15.5C22.0359 11.6141 18.8859 8.46405 15 8.46405Z"
                            fill="url(#paint0_linear_18867_753)"
                          />
                          <path
                            fill-rule="evenodd"
                            clip-rule="evenodd"
                            d="M15 28.8333C22.3638 28.8333 28.3333 22.8638 28.3333 15.5C28.3333 8.1362 22.3638 2.16667 15 2.16667C7.6362 2.16667 1.66667 8.1362 1.66667 15.5C1.66667 22.8638 7.6362 28.8333 15 28.8333ZM15 30.5C23.2843 30.5 30 23.7843 30 15.5C30 7.21573 23.2843 0.5 15 0.5C6.71573 0.5 0 7.21573 0 15.5C0 23.7843 6.71573 30.5 15 30.5Z"
                            fill="url(#paint1_linear_18867_753)"
                          />
                        </g>
                        <defs>
                          <linearGradient
                            id="paint0_linear_18867_753"
                            x1="15"
                            y1="0.5"
                            x2="15"
                            y2="30.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint1_linear_18867_753"
                            x1="15"
                            y1="0.5"
                            x2="15"
                            y2="30.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <clipPath id="clip0_18867_753">
                            <rect
                              width="30"
                              height="30"
                              fill="white"
                              transform="translate(0 0.5)"
                            />
                          </clipPath>
                        </defs>
                      </svg>

                      <svg
                        height="30px"
                        width="30px"
                        version="1.1"
                        id="Layer_1"
                        xmlns="http://www.w3.org/2000/svg"
                        xmlns:xlink="http://www.w3.org/1999/xlink"
                        viewBox="0 0 496.158 496.158"
                        xml:space="preserve"
                        fill="#000000"
                      >
                        <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                        <g
                          id="SVGRepo_tracerCarrier"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        ></g>
                        <g id="SVGRepo_iconCarrier">
                          <path
                            style="fill: #334d5c"
                            d="M248.082,0.003C111.07,0.003,0,111.063,0,248.085c0,137.001,111.07,248.07,248.082,248.07 c137.006,0,248.076-111.069,248.076-248.07C496.158,111.062,385.088,0.003,248.082,0.003z"
                          ></path>
                          <path
                            style="fill: #f2c900"
                            d="M322.377,80.781c10.1,22.706,15.721,47.844,15.721,74.298c0,101.079-81.94,183.019-183.019,183.019 c-26.454,0-51.591-5.622-74.298-15.721c28.49,64.053,92.674,108.721,167.298,108.721c101.078,0,183.019-81.94,183.019-183.019 C431.098,173.454,386.43,109.27,322.377,80.781z"
                          ></path>
                          <g>
                            <path
                              style="fill: #dbbb00"
                              d="M155.079,338.098c-26.454,0-51.591-5.622-74.298-15.721 c28.49,64.053,92.674,108.721,167.298,108.721c101.078,0,183.019-81.94,183.019-183.019 C431.098,248.079,256.157,338.098,155.079,338.098z"
                            ></path>
                            <polygon
                              style="fill: #dbbb00"
                              points="236.634,188.671 209.692,187.721 201.228,162.948 192.765,187.721 165.823,188.671 187.533,203.82 179.347,230.293 201.228,213.77 223.109,230.293 214.924,203.82 "
                            ></polygon>
                          </g>
                          <polygon
                            style="fill: #f2c900"
                            points="209.824,194.758 214.465,177.15 199.799,187.941 183.881,178.107 190.219,195.371 175.339,207.49 194.323,206.778 200.644,224.693 206.441,206.399 224.826,205.941 "
                          ></polygon>
                          <polygon
                            style="fill: #dbbb00"
                            points="101.521,229.699 82.134,229.015 76.043,211.187 69.952,229.015 50.564,229.699 66.187,240.6 60.296,259.651 76.043,247.761 91.789,259.651 85.898,240.6 "
                          ></polygon>
                          <polygon
                            style="fill: #f2c900"
                            points="82.228,234.079 85.568,221.408 75.014,229.174 63.558,222.096 68.12,234.52 57.412,243.241 71.074,242.729 75.623,255.621 79.795,242.456 93.024,242.127 "
                          ></polygon>
                          <polygon
                            style="fill: #dbbb00"
                            points="278.639,68.596 255.368,67.775 248.058,46.377 240.747,67.775 217.476,68.596 236.228,81.682 229.156,104.548 248.058,90.276 266.958,104.548 259.887,81.682 "
                          ></polygon>
                          <polygon
                            style="fill: #f2c900"
                            points="255.482,73.853 259.491,58.644 246.822,67.966 233.072,59.471 238.549,74.382 225.694,84.85 242.093,84.236 247.554,99.71 252.561,83.909 268.44,83.513 "
                          ></polygon>
                        </g>
                      </svg>
                    </label>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="drawer-side">
        <label
          for="my-drawer-3"
          aria-label="close sidebar"
          class="drawer-overlay"
        />
        <ul class="menu bg-base-200 min-h-full w-80 p-4">
          <!-- Sidebar content here -->
          <li><a>Sidebar Item 1</a></li>
          <li><a>Sidebar Item 2</a></li>
        </ul>
      </div>
    </div>
  </header>
</template>

<style>
.bg-gold {
  background: linear-gradient(90deg, #f8e889 0%, #e4b764 100%);
}

.black-gd {
  background: linear-gradient(180deg, #5c5c5c 0%, #000000 100%);
  border: 1px solid var(--Color-3, rgba(26, 26, 26, 1));
  box-shadow: 0px 5px 11px 0px var(--BlackalphaBlack10);
  box-shadow: 0px 20px 20px 0px var(--BlackalphaBlack9);
  box-shadow: 0px 45px 27px 0px var(--BlackalphaBlack5);
  box-shadow: 0px 79px 32px 0px var(--Color-sdsdColor-sd11);
}

.text-gold {
  background: linear-gradient(to right, #f8e889, #e4b764);
  background-clip: text;
  color: transparent;
}
</style>
