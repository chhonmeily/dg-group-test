<template>
  <header>
    <div class="drawer">
      <!-- eslint-disable-next-line vue/html-self-closing -->
      <input id="my-drawer-3" type="checkbox" class="drawer-toggle hidden" />
      <div class="drawer-content flex flex-col relative font-bold">
        <div
          class="hidden xl:block w-[25%] h-[107px] absolute top-0 left-0 rounded-r-full bg-black text-right text-white pr-[20px]"
        >
          <h1 class="text-[76px] mt-[0px] uppercase">
            <a href="/">Logo</a>
          </h1>
        </div>
        <NavbarTop />
        <NavbarBottom />
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
