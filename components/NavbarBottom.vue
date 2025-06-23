<script setup>
import NewsIcon from "~/assets/news-icon.svg";
import ReelsIcon from "~/assets/reels-icon.svg";
import HighLigthIcon from "~/assets/highlight-icon.svg";
import TipIcon from "~/assets/tip-icon.svg";
import VideoIcon from "~/assets/video-icon.svg";
import ComicIcon from "~/assets/comic-icon.svg";
import SunIcon from "~/assets/sun-icon.svg";
import MoonIcon from "~/assets/moon-icon.svg";
</script>
<template>
  <div class="w-full bg-black">
    <div class="@container">
      <div class="max-w-7xl mx-auto">
        <!-- Navbar -->
        <div class="navbar hidden xl:flex">
          <div class="navbar-start" />
          <div class="navbar-center flex-none">
            <ul class="menu menu-horizontal">
              <!-- Navbar menu content here -->
              <li class="text-gold">
                <a>
                  <NewsIcon class="icon-32" />
                  Bảng Tin
                </a>
              </li>
              <li class="text-gold">
                <a>
                  <ReelsIcon class="icon-32" />
                  Reels
                </a>
              </li>
              <li class="text-gold">
                <a>
                  <HighLigthIcon class="icon-32" />
                  Highlight
                </a>
              </li>
              <li class="text-gold">
                <a>
                  <TipIcon class="icon-32" />
                  Tip Kèo
                </a>
              </li>
              <li class="text-gold">
                <a>
                  <VideoIcon class="icon-32" />
                  Phim Ảnh</a
                >
              </li>
              <li class="text-gold">
                <a>
                  <ComicIcon class="icon-32" />
                  Truyện Tranh</a
                >
              </li>
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
              <label class="toggle toggle-neutral w-[60px] text-base-content">
                <input type="checkbox" />
                <SunIcon class="icon-gradient icon-32" />

                <MoonIcon class="icon-32" />
              </label>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.icon-32 {
  width: 32px;
  height: 32px;
}

.icon-32 path {
  fill: #f8e889;
}
</style>
