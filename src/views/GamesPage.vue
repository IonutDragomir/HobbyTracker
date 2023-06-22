<template>
  <div class="container">
    <section class="d-flex justify-content-between my-2">
      <h2>Upcoming games</h2>

      <div class="dropdown">
        <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton1" data-bs-toggle="dropdown"
          aria-expanded="false">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-list-ul"
            viewBox="0 0 16 16">
            <path fill-rule="evenodd"
              d="M5 11.5a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5zm-3 1a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm0 4a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm0 4a1 1 0 1 0 0-2 1 1 0 0 0 0 2z" />
          </svg> Sort
        </button>
        <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
          <li><a class="dropdown-item" href="#">
              Name
              <span v-if="ascending" @click="ascending = false">
                (A - Z)
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-up"
                  viewBox="0 0 16 16">
                  <path fill-rule="evenodd"
                    d="M8 15a.5.5 0 0 0 .5-.5V2.707l3.146 3.147a.5.5 0 0 0 .708-.708l-4-4a.5.5 0 0 0-.708 0l-4 4a.5.5 0 1 0 .708.708L7.5 2.707V14.5a.5.5 0 0 0 .5.5z" />
                </svg>
              </span>
              <span v-else @click="ascending = true">
                (A - Z)
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                  class="bi bi-arrow-down" viewBox="0 0 16 16">
                  <path fill-rule="evenodd"
                    d="M8 1a.5.5 0 0 1 .5.5v11.793l3.146-3.147a.5.5 0 0 1 .708.708l-4 4a.5.5 0 0 1-.708 0l-4-4a.5.5 0 0 1 .708-.708L7.5 13.293V1.5A.5.5 0 0 1 8 1z" />
                </svg>
              </span>
            </a></li>
          <li><a class="dropdown-item" href="#">Date</a></li>
          <li><a class="dropdown-item" href="#">Price</a></li>
        </ul>
      </div>
    </section>

    <div class="row d-flex justify-content-center">
      <CardFrame v-for="game in games" :details="game" :key="game.name" class="col-md-2 col-lg-2 mt-4 g-2" />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import CardFrame from "@/components/CardFrame.vue";


export default {
  name: "GamesPage",
  components: {
    CardFrame,
  },
  data() {
    return {
      ascending: true,
      games: [
        {
          name: "Immortals of Aveum",
          imageUrl: "https://ascendantstudios.com/wp-content/uploads/2023/04/std-keyart-2560x1440-1.jpg",
          release_date: "20.07.2023",
          description1: "Immortals of Aveum is an upcoming first-person shooter game.",
          description2: "Summon your power, stop the Everwar, save the realms. Play as Jak as he and Lucium’s elite battlemages race to uncover Aveum’s past to save its future.",
          description3: "Join the Order of the Immortals, the champion protectors of Lucium, and become Jak, an elite Triarch Magnus. Unleash magic spells with deadly skill, and decimate legions of enemies in a game that defies FPS conventions.",
        },
        {
          name: "Assassin's Creed Mirage",
          imageUrl: "https://cdn2.unrealengine.com/breaker-image-1920x1080-1920x1080-9b4788ed14ab.png",
          release_date: "12.10.2023",
          description1: "Assassin's Creed Mirage is an upcoming action-adventure game",
          description2: "Become the most versatile Assassin in franchise history.",
          description3: "In Assassin's Creed Mirage, you are Basim, a cunning street thief with nightmarish visions seeking answers and justice.Join an ancient organisation and come to understand a new creed – one that will change Basim’s fate in ways he never could have imagined.",
        },
        {
          name: "The Crew Motorfest",
          imageUrl: "https://gaming-cdn.com/images/products/10643/orig/the-crew-motorfest-pc-game-cover.jpg?v=1686596472",
          release_date: "14.09.2023",
          description1: "",
          description2: "",
          description3: "",
        },
        {
          name: "Avatar: Frontiers of Pandora",
          imageUrl: "https://blog.playstation.com/tachyon/2023/06/cebcc8ad6e129dc75698fb6ba4831a26b7f40d15.jpg?resize=1088%2C612&crop_strategy=smart",
          release_date: "17.12.2023",
          description1: "",
          description2: "",
          description3: "",
        },
        {
          name: "Cyberpunk 2077: Phantom Liberty",
          imageUrl: "https://media.vandal.net/i/640x360/12-2022/20221294562119_1.jpg",
          release_date: "26.09.2023",
          description1: "",
          description2: "",
          description3: "",
        },
        {
          name: "Star Wars Jedi: Survivor",
          imageUrl: "https://prod.assets.earlygamecdn.com/images/Jedi-Switch.jpg?mtime=1679929137",
          release_date: "28.04.2023",
          description1: "",
          description2: "",
          description3: "",
        },
        {
          name: "Clockwork Revolution",
          imageUrl: "https://ei5t3fq5d7s.exactdn.com/wp-content/uploads/2023/06/Clockwork_Revolution_00-900x600.jpg?strip=all&lossy=1&webp=80&avif=80&ssl=1",
          release_date: "TBA",
          description1: "",
          description2: "",
          description3: "",
        },
        {
          name: "Fable",
          imageUrl: "https://i.ytimg.com/vi/A4XgptlqDP4/mqdefault.jpg",
          release_date: "TBA",
          description1: "",
          description2: "",
          description3: "",
        },
        {
          name: "Avowed",
          imageUrl: "https://cdn.wccftech.com/wp-content/uploads/2022/03/WCCFavowed1-HD-scaled.jpg",
          release_date: "2024",
          description1: "",
          description2: "",
          description3: "",
        },
        {
          name: "Star Wars: Outlaws",
          imageUrl: "https://cdn.vox-cdn.com/thumbor/1wzozuxUOgVcueiriSqre8xzsZ8=/0x0:1080x1080/1400x788/filters:focal(520x343:521x344)/cdn.vox-cdn.com/uploads/chorus_asset/file/24717904/FyWxFnqXgAIIdI4.jpeg",
          release_date: "2024",
          description1: "",
          description2: "",
          description3: "",
        },
        {
          name: "Starfield",
          imageUrl: "https://i0.wp.com/news.xbox.com/en-us/wp-content/uploads/sites/2/2022/06/StarfieldShowcase_HERO-165ee8e45d4141d2d754.jpg?fit=1920%2C1080&ssl=1",
          release_date: "06.09.2023",
          description1: "",
          description2: "",
          description3: "",
        }
      ],
    };
  },
};
</script>
<style scoped lang="scss">
.container {
  max-width: 1510px;

  section {

    h2 {
      text-align: left;
      display: inline-block;
    }

    .dropdown {
      display: inline-block;

      button:hover {
        box-shadow: rgba(0, 0, 0, 0.24) -3px -1px 8px, rgba(0, 0, 0, 0.24) 1px 3px 8px;
      }
    }
  }

}
</style>