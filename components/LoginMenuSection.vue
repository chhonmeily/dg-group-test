<script setup lang="ts">
import PlusIcon from "~/assets/icon-plus.svg";
import CloseIcon from "~/assets/close-icon.svg";
import CalendarIcon from "~/assets/calendar-icon.svg";
import MessageIcon from "~/assets/message-icon.svg";
import NotificationIcon from "~/assets/notification-icon.svg";
function toggleDropdown(e: MouseEvent): void {
  e.preventDefault();
  const dropdown: HTMLElement | null = document.querySelector(".top-up");
  const swap: HTMLElement | null = document.querySelector(".swap");
  const isOpen: boolean =
    dropdown?.classList.contains("dropdown-open") ?? false;

  if (isOpen) {
    dropdown?.classList.remove("dropdown-open");
    swap?.classList.remove("swap-active");
  } else {
    dropdown?.classList.add("dropdown-open");
    swap?.classList.add("swap-active");
  }
}
</script>
<template>
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
            <div class="flex pt-1">
              <div class="top-up-icon mt-1" />
              <span class="amount mt-1">1000</span>
              <label
                id="trigger-dropdown"
                class="btn-top-up btn btn-circle btn-sm swap"
                @click="toggleDropdown"
              >
                <!-- plus icon -->
                <PlusIcon class="icon swap-off fill-current" />

                <!-- close icon -->
                <CloseIcon class="icon swap-on fill-current" />
              </label>
            </div>

            <TopUpDropDownMenuItem />
          </div>
          <!--Notification Menu-->
          <div class="dropdown dropdown-end">
            <div tabindex="0" role="button" class="btn btn-ghost btn-link">
              <div class="indicator">
                <NotificationIcon class="icon icon-fill" />
                <span class="badge badge-sm indicator-item top-indicator"
                  >8</span
                >
              </div>
            </div>
            <div
              tabindex="0"
              class="card card-compact dropdown-content bg-base-100 z-1 mt-3 w-52 shadow"
            >
              <div class="card-body">
                <span class="text-lg font-bold">Notifications</span>
                <span class="text-info">8 Unread</span>
                <div class="card-actions">
                  <button class="btn btn-primary btn-block btn-sm rounded-full">
                    View Notifications
                  </button>
                </div>
              </div>
            </div>
          </div>
          <!--Messages Menu-->
          <div class="dropdown dropdown-end">
            <div tabindex="0" role="button" class="btn btn-ghost btn-link">
              <div class="indicator">
                <MessageIcon class="icon icon-fill" />
                <span class="badge badge-sm indicator-item top-indicator"
                  >8</span
                >
              </div>
            </div>
            <div
              tabindex="0"
              class="card card-compact dropdown-content bg-base-100 z-1 mt-3 w-52 shadow"
            >
              <div class="card-body">
                <span class="text-lg font-bold">Messages</span>
                <span class="text-info">8 Unread Messages</span>
                <div class="card-actions">
                  <button class="btn btn-primary btn-block btn-sm rounded-full">
                    Read Messages
                  </button>
                </div>
              </div>
            </div>
          </div>
          <!--Calendar Menu-->
          <div class="indicator">
            <button class="btn btn-link">
              <CalendarIcon class="icon icon-fill" />
            </button>
          </div>
        </div>
        <!--Profile Menu-->
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
</template>

<style>
.icon-fill path {
  fill: rgba(248, 232, 137, 1);
}

.btn-top-up {
  background: linear-gradient(180deg, #f8e889 0%, #e4b764 100%);
}
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
</style>
