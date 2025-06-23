<template>
  <div class="relative">
    <div class="game-container mx-auto">
      <div
        tabindex="0"
        class="collapse collapse-arrow bg-base-100 border-base-300 border"
      >
        <input type="checkbox" class="peer" checked />
        <div class="collapse-title font-semibold text-right">Thu gọn</div>
        <div class="collapse-content text-sm">
          <div class="grid grid-cols-5 gap-2 p-4">
            <div
              class="card game-card basketball bg-gold w-66 shadow-lg p-1 rounded-3xl relative overflow-hidden"
            >
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
                  <div class="blink-status mr-[5%] mt-2">
                    <img src="~/assets/blink.svg" width="65" />
                  </div>
                </div>
              </div>
            </div>
            <div
              class="card game-card e-sport bg-gold w-66 shadow-lg p-1 rounded-3xl relative overflow-hidden"
            >
              <div class="game-hot absolute top-0 right-0" />
              <figure class="relative overflow-hidden rounded-3xl">
                <img src="~/assets/esport.jpg" alt="game" />
                <div class="game-icon e-sport absolute left-2 bottom-13" />
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
                  <button
                    class="btn btn-lg btn-bell rounded-2xl bg-gold border-gold shadow-lg p-2 mr-[5%] mt-2"
                  >
                    <img class="mx-auto mb-0 p-0" src="~/assets/bell.svg" />
                    <span class="text-xs font-bold">Huỷ lịch</span>
                  </button>
                </div>
              </div>
            </div>
            <div
              class="card game-card football bg-gold w-66 shadow-lg p-1 rounded-3xl relative overflow-hidden"
            >
              <div class="game-hot absolute top-0 right-0" />
              <figure class="relative overflow-hidden rounded-3xl">
                <img src="~/assets/football-match-resize.jpg" alt="game" />
                <div class="game-icon football absolute left-2 bottom-13" />
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
                  <button
                    class="btn btn-lg btn-bell black-gd transparent rounded-2xl shadow-lg p-2 mr-[5%] mt-2"
                  >
                    <img
                      class="mx-auto mb-0 p-0"
                      src="~/assets/bell-full.svg"
                    />
                    <span class="text-xs font-bold text-gold">Đặt lịch</span>
                  </button>
                </div>
              </div>
            </div>
            <div
              class="card game-card basketball bg-gold w-66 shadow-lg p-1 rounded-3xl relative overflow-hidden"
            >
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
                  <button
                    class="btn btn-lg btn-bell black-gd transparent rounded-2xl shadow-lg p-2 mr-[5%] mt-2"
                  >
                    <img
                      class="mx-auto mb-0 p-0"
                      src="~/assets/bell-full.svg"
                    />
                    <span class="text-xs font-bold text-gold">Đặt lịch</span>
                  </button>
                </div>
              </div>
            </div>
            <div
              class="card game-card e-sport bg-gold w-66 shadow-lg p-1 rounded-3xl relative overflow-hidden"
            >
              <div class="game-hot absolute top-0 right-0" />
              <figure class="relative overflow-hidden rounded-3xl">
                <img src="~/assets/esport.jpg" alt="game" />
                <div class="game-icon e-sport absolute left-2 bottom-13" />
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
                  <button
                    class="btn btn-lg btn-bell black-gd transparent rounded-2xl shadow-lg p-2 mr-[5%] mt-2"
                  >
                    <img
                      class="mx-auto mb-0 p-0"
                      src="~/assets/bell-full.svg"
                    />
                    <span class="text-xs font-bold text-gold">Đặt lịch</span>
                  </button>
                </div>
              </div>
            </div>
            <div
              class="card game-card basketball bg-gold w-66 shadow-lg p-1 rounded-3xl relative overflow-hidden"
            >
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
                  <div class="blink-status mr-[5%] mt-2">
                    <img src="~/assets/blink.svg" width="65" />
                  </div>
                </div>
              </div>
            </div>
            <div
              class="card game-card e-sport bg-gold w-66 shadow-lg p-1 rounded-3xl relative overflow-hidden"
            >
              <div class="game-hot absolute top-0 right-0" />
              <figure class="relative overflow-hidden rounded-3xl">
                <img src="~/assets/esport.jpg" alt="game" />
                <div class="game-icon e-sport absolute left-2 bottom-13" />
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
                  <button
                    class="btn btn-lg btn-bell rounded-2xl bg-gold border-gold shadow-lg p-2 mr-[5%] mt-2"
                  >
                    <img class="mx-auto mb-0 p-0" src="~/assets/bell.svg" />
                    <span class="text-xs font-bold">Huỷ lịch</span>
                  </button>
                </div>
              </div>
            </div>
            <div
              class="card game-card football bg-gold w-66 shadow-lg p-1 rounded-3xl relative overflow-hidden"
            >
              <div class="game-hot absolute top-0 right-0" />
              <figure class="relative overflow-hidden rounded-3xl">
                <img src="~/assets/football-match-resize.jpg" alt="game" />
                <div class="game-icon football absolute left-2 bottom-13" />
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
                  <button
                    class="btn btn-lg btn-bell black-gd transparent rounded-2xl shadow-lg p-2 mr-[5%] mt-2"
                  >
                    <img
                      class="mx-auto mb-0 p-0"
                      src="~/assets/bell-full.svg"
                    />
                    <span class="text-xs font-bold text-gold">Đặt lịch</span>
                  </button>
                </div>
              </div>
            </div>
            <div
              class="card game-card basketball bg-gold w-66 shadow-lg p-1 rounded-3xl relative overflow-hidden"
            >
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
                  <button
                    class="btn btn-lg btn-bell black-gd transparent rounded-2xl shadow-lg p-2 mr-[5%] mt-2"
                  >
                    <img
                      class="mx-auto mb-0 p-0"
                      src="~/assets/bell-full.svg"
                    />
                    <span class="text-xs font-bold text-gold">Đặt lịch</span>
                  </button>
                </div>
              </div>
            </div>
            <div
              class="card game-card e-sport bg-gold w-66 shadow-lg p-1 rounded-3xl relative overflow-hidden"
            >
              <div class="game-hot absolute top-0 right-0" />
              <figure class="relative overflow-hidden rounded-3xl">
                <img src="~/assets/esport.jpg" alt="game" />
                <div class="game-icon e-sport absolute left-2 bottom-13" />
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
                  <button
                    class="btn btn-lg btn-bell black-gd transparent rounded-2xl shadow-lg p-2 mr-[5%] mt-2"
                  >
                    <img
                      class="mx-auto mb-0 p-0"
                      src="~/assets/bell-full.svg"
                    />
                    <span class="text-xs font-bold text-gold">Đặt lịch</span>
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
