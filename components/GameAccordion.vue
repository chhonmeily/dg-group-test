<template>
  <div class="relative">
    <div class="game-container mx-auto mt-[40px]">
      <div
        tabindex="0"
        class="collapse collapse-arrow bg-base-100 border-base-300 border"
      >
        <input type="checkbox" class="peer" checked />
        <div class="collapse-title font-semibold text-right">Thu gọn</div>
        <div class="collapse-content text-sm">
          <div class="grid grid-cols-5 gap-2 p-4">
            <GameBasketball />
            <GameEsport />
            <GameFootball />
            <GameBasketball />
            <GameEsport />
            <GameBasketball />
            <GameEsport />
            <GameFootball />
            <GameBasketball />
            <GameEsport />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
