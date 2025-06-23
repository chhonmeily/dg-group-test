<script setup lang="ts">
import { onMounted } from "vue";

function scrollGame(): void {
  const slider: HTMLElement | null = document.querySelector("#game-carousel"); // Select your scrollable container

  let isDown: boolean = false;
  let startX: number;
  let scrollLeft: number;

  if (slider) {
    slider.addEventListener("mousedown", (e: MouseEvent) => {
      isDown = true;
      slider.classList.add("active"); // Optional: Add a class for styling when dragging
      startX = e.pageX - slider.offsetLeft;
      scrollLeft = slider.scrollLeft;
    });

    slider.addEventListener("mouseleave", () => {
      isDown = false;
      slider.classList.remove("active");
    });

    slider.addEventListener("mouseup", () => {
      isDown = false;
      slider.classList.remove("active");
    });

    slider.addEventListener("mousemove", (e: MouseEvent) => {
      if (!isDown) return; // Stop the function from running when not clicked
      e.preventDefault(); // Prevent default browser drag behavior
      const x: number = e.pageX - slider.offsetLeft;
      const walk: number = x - startX; // The distance the mouse has moved
      slider.scrollLeft = scrollLeft - walk;
    });

    const card: HTMLElement | null = slider.querySelector(".card");
    const btnNext: HTMLElement | null = document.querySelector(".btn-next");
    const btnPrevious: HTMLElement | null =
      document.querySelector(".btn-previous");

    if (btnNext && card) {
      btnNext.addEventListener("click", () => {
        slider.scrollLeft += card.offsetLeft;
      });
    }

    if (btnPrevious && card) {
      btnPrevious.addEventListener("click", () => {
        slider.scrollLeft -= card.offsetLeft;
      });
    }
  }
}

onMounted(() => {
  scrollGame();
});
</script>

<template>
  <div
    class="game-container mx-auto flex justify-end-safe bg-base-200 rounded mt-3 p-2"
  >
    <a class="link link-hover flex items-center font-bold"
      >Xem tất cả
      <img src="@/assets/caret.svg?url" />
    </a>
  </div>
  <div class="flex items-center relative">
    <button
      aria-label="previous"
      class="btn btn-link btn-previous absolute left-[9.5%] z-1"
    >
      <img src="~/assets/btn-previous.svg?url" />
    </button>
    <div id="game-carousel" class="game-container mx-auto">
      <div class="flex items-center gap-4 p-4">
        <GameBasketball />
        <GameEsport />
        <GameFootball />
        <GameBasketball />
        <GameEsport />
        <GameFootball />
        <GameBasketball />
      </div>
    </div>
    <button
      aria-label="next"
      class="btn btn-link btn-next absolute right-[9.5%] z-1"
    >
      <img src="~/assets/btn-next.svg?url" />
    </button>
  </div>
</template>

<style>
.game-hot {
  background: url("~/assets/hot.png");
  width: 77px;
  height: 64px;
  z-index: 1;
}

.game-icon {
  background: url("~/assets/game-type.png");
  display: block;
  width: 40px;
  height: 40px;
  background-size: 100%;
  background-position-y: 0;
}

.game-icon.basketball {
  background-position-y: 0;
}

.game-icon.e-sport {
  background-position-y: -82px;
}

.game-icon.football {
  background-position-y: -44px;
}

.blink-status {
  animation: blink-animation 1s steps(1, end) infinite; /* 1 second duration, step function, infinite loop */
}

@keyframes blink-animation {
  0%,
  50% {
    opacity: 1;
  }
  50%,
  100% {
    opacity: 0;
  }
}

.game-container {
  width: 1440px;
  display: flex;
  overflow-x: scroll;
}

.btn-bell {
  display: block;
  margin: 0;
  line-height: 5px;
}

.btn-bell span {
  line-height: 0;
}
.game-card h1,
.game-card h2,
.game-card h3,
.game-card h4,
.game-card h5,
.game-card h6 {
  margin-block-start: 0;
  margin-block-end: 0;
  margin-inline-start: 0;
  margin-inline-end: 0;
  line-height: 16px;
}

.bg-gold {
  background: linear-gradient(180deg, #f8e889 0%, #e4b764 100%);
}

.border-gold {
  border: 1px solid;
  border-color: rgba(228, 183, 100, 1);
}
</style>
