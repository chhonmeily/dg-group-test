<script setup>
function toggleDropdown(e) {
  e.preventDefault();
  const dropdown = document.querySelector(".top-up");
  const swap = document.querySelector(".swap");
  const isOpen = dropdown.classList.contains("dropdown-open");

  if (isOpen) {
    dropdown.classList.remove("dropdown-open");
    swap.classList.remove("swap-active");
  } else {
    dropdown.classList.add("dropdown-open");
    swap.classList.add("swap-active");
  }
}
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
          <div class="navbar-center pt-4">
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
          <div class="navbar-end uppercase flex hidden">
            <a
              class="btn btn-sm rounded-full mx-1 border-white shadow-xl shadow-black/20"
              >đăng ký</a
            >
            <a class="btn btn-sm rounded-full mx-1 black-gd">
              <span class="text-gold">đăng nhập</span>
            </a>
          </div>
          <!--After User Logged In -->
          <div class="login-section flex">
            <div class="grid">
              <div class="welcome text-[10px] text-center">
                <span class="welcome-text">Xin chào, NguyenVanDen</span>
              </div>
              <div class="flex bg-neutral rounded-full">
                <div class="flex pt-2 pb-2">
                  <div
                    class="dropdown dropdown-center top-up bg-white rounded-full ml-2"
                  >
                    <div class="flex">
                      <div class="top-up-icon icon-coin-1" />
                      <span class="amount">1000</span>
                      <label
                        id="trigger-dropdown"
                        class="btn-top-up btn btn-circle btn-sm btn-warning swap"
                        @click="toggleDropdown"
                      >
                        <!-- plus icon -->
                        <svg
                          class="swap-off fill-current"
                          fill="#000000"
                          width="24"
                          height="24"
                          viewBox="0 0 24 24"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                          <g
                            id="SVGRepo_tracerCarrier"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                          ></g>
                          <g id="SVGRepo_iconCarrier">
                            <path
                              fill-rule="evenodd"
                              d="M11.75 4.5a.75.75 0 01.75.75V11h5.75a.75.75 0 010 1.5H12.5v5.75a.75.75 0 01-1.5 0V12.5H5.25a.75.75 0 010-1.5H11V5.25a.75.75 0 01.75-.75z"
                            ></path>
                          </g>
                        </svg>

                        <!-- close icon -->
                        <svg
                          class="swap-on fill-current"
                          xmlns="http://www.w3.org/2000/svg"
                          width="24"
                          height="24"
                          viewBox="0 0 512 512"
                        >
                          <polygon
                            points="400 145.49 366.51 112 256 222.51 145.49 112 112 145.49 222.51 256 112 366.51 145.49 400 256 289.49 366.51 400 400 366.51 289.49 256 400 145.49"
                          />
                        </svg>
                      </label>
                    </div>

                    <TopUpDropDownMenuItem />
                  </div>
                  <div class="dropdown dropdown-end">
                    <div
                      tabindex="0"
                      role="button"
                      class="btn btn-ghost btn-link"
                    >
                      <div class="indicator">
                        <svg
                          width="22"
                          height="23"
                          viewBox="0 0 22 23"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <g clip-path="url(#clip0_18905_1646)">
                            <path
                              d="M8.7594 19.4507C9.30931 19.3344 12.6601 19.3344 13.21 19.4507C13.6801 19.5593 14.1885 19.813 14.1885 20.3669C14.1611 20.8943 13.8517 21.3618 13.4243 21.6587C12.87 22.0908 12.2195 22.3644 11.5395 22.463C11.1635 22.5118 10.7939 22.5129 10.431 22.463C9.74988 22.3644 9.0994 22.0908 8.54622 21.6576C8.11767 21.3618 7.80828 20.8943 7.78094 20.3669C7.78094 19.813 8.28931 19.5593 8.7594 19.4507ZM11.0496 0.5C13.3378 0.5 15.6752 1.58572 17.0636 3.38713C17.9644 4.54708 18.3777 5.70592 18.3777 7.50733V7.97596C18.3777 9.35749 18.7428 10.1718 19.5464 11.1102C20.1553 11.8015 20.3499 12.6889 20.3499 13.6516C20.3499 14.6133 20.034 15.5262 19.401 16.2673C18.5723 17.1558 17.4036 17.7231 16.2109 17.8217C14.4824 17.969 12.7529 18.0931 11.0005 18.0931C9.24688 18.0931 7.51846 18.0189 5.79003 17.8217C4.5962 17.7231 3.42752 17.1558 2.59993 16.2673C1.96694 15.5262 1.6499 14.6133 1.6499 13.6516C1.6499 12.6889 1.84559 11.8015 2.45344 11.1102C3.28212 10.1718 3.62321 9.35749 3.62321 7.97596V7.50733C3.62321 5.65717 4.08457 4.44737 5.0346 3.26305C6.44707 1.53587 8.71119 0.5 10.9513 0.5H11.0496Z"
                              fill="url(#paint0_linear_18905_1646)"
                            />
                          </g>
                          <defs>
                            <linearGradient
                              id="paint0_linear_18905_1646"
                              x1="10.9999"
                              y1="0.5"
                              x2="10.9999"
                              y2="22.5"
                              gradientUnits="userSpaceOnUse"
                            >
                              <stop stop-color="#F8E889" />
                              <stop offset="1" stop-color="#E4B764" />
                            </linearGradient>
                            <clipPath id="clip0_18905_1646">
                              <rect
                                width="22"
                                height="22"
                                fill="white"
                                transform="translate(0 0.5)"
                              />
                            </clipPath>
                          </defs>
                        </svg>

                        <span
                          class="badge badge-sm indicator-item top-indicator"
                          >8</span
                        >
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
                      class="btn btn-ghost btn-link"
                    >
                      <div class="indicator">
                        <svg
                          width="22"
                          height="23"
                          viewBox="0 0 22 15"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M0.701557 1.7384L9.86822 6.66274C10.1762 6.82774 10.5747 6.90596 10.9756 6.90596C11.3764 6.90596 11.7749 6.82774 12.0829 6.66274L21.2496 1.7384C21.8472 1.41696 22.4119 0.166626 21.3156 0.166626H0.63678C-0.459553 0.166626 0.105113 1.41696 0.701557 1.7384ZM21.527 4.43096L12.0829 9.35285C11.6673 9.5704 11.3764 9.59607 10.9756 9.59607C10.5747 9.59607 10.2838 9.5704 9.86822 9.35285C9.45267 9.13529 1.15011 4.78296 0.47178 4.42974C-0.00488688 4.1804 1.97519e-06 4.47251 1.97519e-06 4.6974V13.6111C1.97519e-06 14.1244 0.69178 14.8333 1.22222 14.8333H20.7778C21.3082 14.8333 22 14.1244 22 13.6111V4.69863C22 4.47374 22.0049 4.18163 21.527 4.43096Z"
                            fill="url(#paint0_linear_18905_1654)"
                          />
                          <defs>
                            <linearGradient
                              id="paint0_linear_18905_1654"
                              x1="11"
                              y1="0.166626"
                              x2="11"
                              y2="14.8333"
                              gradientUnits="userSpaceOnUse"
                            >
                              <stop stop-color="#F8E889" />
                              <stop offset="1" stop-color="#E4B764" />
                            </linearGradient>
                          </defs>
                        </svg>

                        <span
                          class="badge badge-sm indicator-item top-indicator"
                          >8</span
                        >
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
                  <div class="indicator">
                    <button class="btn btn-link">
                      <svg
                        width="22"
                        height="23"
                        viewBox="0 0 22 23"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <g clip-path="url(#clip0_18905_1658)">
                          <g clip-path="url(#clip1_18905_1658)">
                            <path
                              d="M21.4501 17.275C21.4501 19.8569 19.357 21.95 16.7751 21.95C14.1932 21.95 12.1001 19.8569 12.1001 17.275C12.1001 14.693 14.1932 12.6 16.7751 12.6C19.357 12.6 21.4501 14.693 21.4501 17.275Z"
                              fill="url(#paint0_linear_18905_1658)"
                            />
                            <path
                              d="M7.92166 14.0476L5.72122 14.0456L5.71264 15.6576L7.9221 15.6609L7.92166 14.0476Z"
                              fill="url(#paint1_linear_18905_1658)"
                            />
                            <path
                              d="M2.65046 16.476L2.64298 18.0914H4.8531L4.85244 16.4757L2.65046 16.476Z"
                              fill="url(#paint2_linear_18905_1658)"
                            />
                            <path
                              d="M4.84188 14.0456H2.64738L2.64298 15.649C2.7961 15.6925 4.54136 15.6611 4.85244 15.6611C4.85244 15.4426 4.86938 14.1464 4.84188 14.0456Z"
                              fill="url(#paint3_linear_18905_1658)"
                            />
                            <path
                              d="M5.71286 11.6153L5.7133 13.2294L7.91638 13.2307L7.92232 11.6206L5.71286 11.6153Z"
                              fill="url(#paint4_linear_18905_1658)"
                            />
                            <path
                              d="M5.71286 18.0883L7.9221 18.091L7.92188 16.4788L5.71748 16.476L5.71286 18.0883Z"
                              fill="url(#paint5_linear_18905_1658)"
                            />
                            <path
                              d="M13.397 3.81761C13.7926 4.52447 14.9951 4.33769 15.084 3.53161C15.1014 3.37409 15.0884 2.42985 15.0884 2.19181C15.0884 1.84179 15.1458 1.21501 14.992 0.941547C14.8426 0.675567 14.4805 0.430047 14.0132 0.520027C13.6428 0.591087 13.346 0.859487 13.3051 1.22909C13.2872 1.38947 13.3 2.32667 13.3 2.56603C13.3 2.91693 13.2435 3.54349 13.397 3.81761Z"
                              fill="url(#paint6_linear_18905_1658)"
                            />
                            <path
                              d="M8.79154 15.6598L10.9816 15.6578L10.981 14.052H8.79154V15.6598Z"
                              fill="url(#paint7_linear_18905_1658)"
                            />
                            <path
                              d="M4.85442 13.17L4.85266 11.6155C4.5297 11.6155 2.81194 11.5812 2.64342 11.6272L2.64386 13.2259L4.84364 13.2312L4.85442 13.17Z"
                              fill="url(#paint8_linear_18905_1658)"
                            />
                            <path
                              d="M17.1306 9.18517H14.9201L14.9192 10.7359L14.9234 10.8006H17.1254L17.132 10.7359L17.1306 9.18517Z"
                              fill="url(#paint9_linear_18905_1658)"
                            />
                            <path
                              d="M19.7627 12.5314C19.4547 12.3501 19.1307 12.1996 18.7952 12.0812C18.7736 11.2228 18.8077 7.86495 18.7866 7.72283L0.980662 7.72811L0.989682 19.4653L11.6357 19.4666C11.7519 19.7762 11.8951 20.0749 12.0645 20.3598C11.2305 20.3618 10.1802 20.3484 9.67198 20.3484H1.80786C1.4123 20.3484 1.15556 20.3684 0.816982 20.2294C0.544402 20.1176 0.359162 19.9423 0.222542 19.7474C0.0425822 19.4917 0.0131023 19.2675 0.0131023 18.9226V4.65977C0.0131023 4.01253 -0.0909578 3.34395 0.287442 2.88943C0.755602 2.32755 1.31396 2.37837 1.97682 2.37837H4.214C4.2184 2.52621 4.2393 2.56383 4.1568 2.65425C3.73462 3.11669 3.66268 3.77185 3.92558 4.32207C4.16296 4.81839 4.77016 5.29359 5.5802 5.29359C6.92484 5.29359 7.86314 3.97711 7.13406 2.82519C6.95058 2.53545 6.93342 2.69451 6.9442 2.37837H12.8299C12.8402 2.68307 12.8349 2.52247 12.633 2.83465C11.9305 3.91969 12.8006 5.29425 14.1952 5.29359C15.5473 5.29315 16.4759 3.97249 15.7497 2.82475C15.566 2.53413 15.5471 2.69297 15.5583 2.37837H17.6485C18.3877 2.37837 18.899 2.33129 19.3366 2.73741C19.4008 2.79703 19.409 2.79615 19.4624 2.86171C19.5891 3.01791 19.6675 3.13495 19.7216 3.34109C19.788 3.59343 19.761 3.96259 19.761 4.23429C19.761 4.23429 19.7766 11.232 19.7627 12.5314Z"
                              fill="url(#paint10_linear_18905_1658)"
                            />
                            <path
                              d="M4.77544 3.80705C4.91932 4.07303 5.29046 4.32867 5.75862 4.24199C6.13042 4.17313 6.4195 3.89923 6.46724 3.54393C6.48682 3.39697 6.4745 2.43711 6.4745 2.20875C6.4745 1.85741 6.53346 1.23349 6.38298 0.953427C6.23976 0.686347 5.87148 0.432467 5.40992 0.516287C5.03526 0.584267 4.73804 0.852667 4.69162 1.21457C4.67402 1.35317 4.68634 2.32667 4.68634 2.54931C4.68634 2.88899 4.6331 3.54371 4.77544 3.80705Z"
                              fill="url(#paint11_linear_18905_1658)"
                            />
                            <path
                              d="M13.131 13.231L11.9241 13.2312L11.8524 13.2292L11.8522 11.6155L14.0614 11.6197L14.0577 12.5441L13.131 13.231Z"
                              fill="url(#paint12_linear_18905_1658)"
                            />
                            <path
                              d="M13.9886 10.8006L14.0581 10.7989L14.0612 9.18869L11.852 9.18517L11.8522 10.7984L11.9241 10.8011L13.9886 10.8006Z"
                              fill="url(#paint13_linear_18905_1658)"
                            />
                            <path
                              d="M10.9816 11.6186L8.79154 11.6168L8.7933 13.2252H10.9816V11.6186Z"
                              fill="url(#paint14_linear_18905_1658)"
                            />
                            <path
                              d="M16.899 22.5C15.537 22.5 14.2559 21.9652 13.2919 20.9939C12.3287 20.0257 11.7981 18.7358 11.7981 17.3623C11.7981 15.9889 12.3285 14.6979 13.2919 13.7275C14.2561 12.7575 15.5372 12.2234 16.899 12.2234C18.2608 12.2234 19.5418 12.7575 20.5061 13.7275C21.4695 14.6979 21.9999 15.9887 21.9999 17.3623C21.9999 18.736 21.4693 20.0257 20.5061 20.9941C19.5421 21.9652 18.261 22.5 16.899 22.5ZM16.899 13.2853C15.8192 13.2853 14.803 13.7088 14.0381 14.4781C13.274 15.2477 12.8532 16.272 12.8532 17.3623C12.8532 18.4527 13.274 19.4743 14.0381 20.2432C14.8024 21.0137 15.8183 21.4378 16.8988 21.4378C17.9792 21.4378 18.9954 21.0137 19.7594 20.2432C20.5235 19.4728 20.9443 18.4496 20.9443 17.3621C20.9443 16.2747 20.5235 15.2488 19.7594 14.4779C18.9947 13.7088 17.979 13.2853 16.899 13.2853Z"
                              fill="url(#paint15_linear_18905_1658)"
                            />
                            <path
                              d="M19.9489 15.3153C19.8334 15.1764 19.6745 15.0957 19.5091 15.0763C19.3885 15.0618 19.2645 15.0801 19.1507 15.1324C19.0959 15.1573 19.0438 15.1899 18.9954 15.2303L15.7986 17.9L14.9613 17.1899C14.7078 16.976 14.3439 16.9824 14.0975 17.1864C14.0654 17.213 14.0353 17.2429 14.0078 17.2759C13.8043 17.5208 13.801 17.8666 13.9792 18.1132C14.0111 18.1574 14.0489 18.1984 14.0923 18.2351L15.3647 19.3127C15.572 19.4867 15.8525 19.5148 16.083 19.4079C16.1398 19.382 16.1937 19.3474 16.2425 19.3052L19.8651 16.2756C19.9524 16.2019 20.0166 16.1103 20.0571 16.0107C20.0672 15.986 20.0756 15.9607 20.0826 15.9354C20.1401 15.7267 20.0974 15.4939 19.9489 15.3153Z"
                              fill="#F8E889"
                            />
                          </g>
                        </g>
                        <defs>
                          <linearGradient
                            id="paint0_linear_18905_1658"
                            x1="16.7751"
                            y1="12.6"
                            x2="16.7751"
                            y2="21.95"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#FF6761" />
                            <stop offset="1" stop-color="#FF1D1D" />
                          </linearGradient>
                          <linearGradient
                            id="paint1_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint2_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint3_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint4_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint5_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint6_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint7_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint8_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint9_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint10_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint11_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint12_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint13_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint14_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <linearGradient
                            id="paint15_linear_18905_1658"
                            x1="11"
                            y1="0.5"
                            x2="11"
                            y2="22.5"
                            gradientUnits="userSpaceOnUse"
                          >
                            <stop stop-color="#F8E889" />
                            <stop offset="1" stop-color="#E4B764" />
                          </linearGradient>
                          <clipPath id="clip0_18905_1658">
                            <rect
                              width="22"
                              height="22"
                              fill="white"
                              transform="translate(0 0.5)"
                            />
                          </clipPath>
                          <clipPath id="clip1_18905_1658">
                            <rect
                              width="30"
                              height="30"
                              fill="white"
                              transform="translate(0 0.5)"
                            />
                          </clipPath>
                        </defs>
                      </svg>
                    </button>
                  </div>
                </div>
                <div class="dropdown dropdown-end">
                  <div
                    tabindex="0"
                    role="button"
                    class="btn btn-ghost btn-link avatar user-profile indicator"
                  >
                    <span
                      class="indicator-item indicator-bottom badge badge-xs avatar-indicator"
                      >20</span
                    >
                    <div class="w-10">
                      <img
                        alt="Tailwind CSS Navbar component"
                        src="https://img.daisyui.com/images/stock/photo-1534528741775-53994a69daeb.webp"
                      />
                    </div>
                  </div>
                  <ProfileDropDownMenuItem />
                </div>
              </div>
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
.top-up-icon {
  background: url("~/assets/top-up-badge.png");
  background-size: cover;
  width: 40px;
  height: 28px;
  background-position-y: 0px;
  display: flex;
}

.login-section .indicator .btn,
.login-section .dropdown .btn {
  margin: 0 5px;
  padding: 0;
}

.login-section .dropdown .btn.user-profile {
  background: url("~/assets/user.png");
  background-size: contain;
  padding: 5px;
  height: auto;
  margin: 0;
}

.login-section .dropdown .btn.user-profile img {
  padding: 2px;
  border-radius: 100%;
  overflow: auto;
}

.login-section .top-indicator {
  border-radius: 100%;
  border: 1px solid #ff1d1d;
  padding: 5px;
  margin: 0;
  background: linear-gradient(180deg, #ff6761 0%, #ff1d1d 100%);
  color: rgba(248, 232, 137, 1);
}

.login-section .avatar-indicator {
  border-radius: 100%;
  border: 2px solid;
  color: rgba(248, 232, 137, 1);
  background: #000;
  min-width: 25px;
  padding: 10px 5px;
  display: inline-flex;
  align-items: center;
}

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
