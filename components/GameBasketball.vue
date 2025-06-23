<template>
  <div
    class="card game-card basketball bg-gold w-66 shadow-lg p-1 rounded-3xl relative overflow-hidden"
  >
    <a href="#">
      <div class="game-hot absolute top-0 right-0" />
      <figure class="relative overflow-hidden rounded-3xl">
        <img src="~/assets/basketball-match.jpg" alt="game" />
        <div class="game-icon basketball absolute left-2 bottom-13" />
      </figure>

      <div
        class="card-body p-0 m-0 bg-gold border-gold absolute bottom-[0px] left-0 w-full rounded-3xl"
      >
        <div class="flex justify-between ml-[15%]">
          <div class="text-center">
            <h2 class="p-0 pt-2 m-0">
              <span class="team-home">Team A </span>
              <span class="font-bold">vs </span>
              <span class="team-away">Team B</span>
            </h2>
            <h3 class="font-bold m-0 p-0 pb-2 uppercase">BLV Noname</h3>
          </div>
        </div>
      </div>
    </a>
    <div class="blink-status absolute bottom-2 right-3">
      <img src="~/assets/blink.svg?url" width="65" />
    </div>
  </div>
</template>
