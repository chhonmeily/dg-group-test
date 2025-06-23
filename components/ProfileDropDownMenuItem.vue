<script lang="ts" setup>
import UserIcon from "~/assets/user-icon.svg";
import HomeIcon from "~/assets/home-icon.svg";
import MissionIcon from "~/assets/mission-icon.svg";
import WalletIcon from "~/assets/wallet-icon.svg";
import HistoryIcon from "~/assets/history-icon.svg";
import LogOutIcon from "~/assets/logout-icon.svg";
</script>
<template>
  <ul
    tabindex="0"
    class="profile-drop-down top-menu-container uppercase dropdown-content menu w-[280px] bg-base-100/50 backdrop-blur rounded-box z-1 w-52 p-2 shadow-sm"
  >
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1">
      <a class="rounded-full">
        <UserIcon class="icon" />
        Trung tâm Tài khoản
      </a>
    </li>
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1">
      <a class="rounded-full">
        <HomeIcon class="icon" />
        Trang cá nhân</a
      >
    </li>
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1">
      <a class="rounded-full">
        <MissionIcon class="icon" />
        Nhiệm vụ</a
      >
    </li>
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1">
      <a class="rounded-full">
        <WalletIcon class="icon" />
        Ví của bạn</a
      >
    </li>
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1">
      <a class="rounded-full">
        <HistoryIcon class="icon" />
        lịch sử giao dịch</a
      >
    </li>
    <li class="bg-base-100/0.5 backdrop-blur rounded-full mb-1">
      <a class="rounded-full">
        <LogOutIcon class="icon" />
        Thoát tài khoản</a
      >
    </li>
  </ul>
</template>

<style>
.profile-drop-down.top-menu-container li:hover a svg path {
  fill: #f8e889;
}

.icon {
  width: 24px;
  height: 24px;
}

.user-icon path {
  fill: #000;
}
</style>
