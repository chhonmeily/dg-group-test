<template>
  <ul
    id="top-up-drop-down"
    tabindex="0"
    class="uppercase dropdown-content menu bg-base-100/50 backdrop-blur rounded-box z-1 w-52 p-2 shadow-sm"
  >
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1">
      <a class="rounded-full"> <span class="menu-icon icon-coin-2" /> 20.000</a>
    </li>
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1">
      <a class="rounded-full"> <span class="menu-icon icon-coin-3" /> 20.000</a>
    </li>
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1 mx-auto">
      <a class="rounded-full">
        <div class="rounded-full btn-top-up">
          <svg
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
        </div>
        Nạp thêm</a
      >
    </li>
  </ul>
</template>

<style>
.btn-top-up {
  background: linear-gradient(180deg, #f8e889 0%, #e4b764 100%);
}

#top-up-drop-down .menu-icon {
  display: block;
  width: 32px;
  height: 27px;
  background: url("~/assets/top-up-badge.png");
  background-position-y: 0;
  background-size: 100%;
}

#top-up-drop-down .icon-coin-2 {
  background-position-y: -21px;
}

#top-up-drop-down .icon-coin-3 {
  background-position-y: -48px;
}
</style>
