<script>
import ToolbarComp from '@/components/ToolbarComp.vue'
import FooterComp from '@/components/FooterComp.vue'

export default {
  name: 'Home',
  components: {
    ToolbarComp,
    FooterComp
  },
  data () {
      return {
        isMobile: false,
        colors: [
          'indigo',
          'warning',
          'pink darken-2',
          'red lighten-1',
          'deep-purple accent-4',
        ],
        tech: [
          { id: 1, title: "Vue.js", icon: "mdi-vuejs", color: "#42b883" },
          { id: 2, title: "Laravel", icon: "mdi-laravel", color: "#f05340" },
          { id: 3, title: "AdonisJS", icon: "mdi-alpha-a-box", color: "#5a2c82" },
          { id: 4, title: "Bootstrap", icon: "mdi-bootstrap", color: "#7952b3" },
          { id: 5, title: "Tailwind CSS", icon: "mdi-tailwind", color: "#38b2ac" },
          { id: 6, title: "PostgreSQL", icon: "mdi-database", color: "#336791" },
          { id: 7, title: "MySQL", icon: "mdi-database", color: "#00758f" },
          { id: 8, title: "JavaScript", icon: "mdi-language-javascript", color: "#f7df1e" },
          { id: 9, title: "TypeScript", icon: "mdi-language-typescript", color: "#007acc" },
          { id: 10, title: "Docker", icon: "mdi-docker", color: "#2496ed" },
        ],
        items: [
          {
            src: '../src/assets/background.svg',
          },
        ],
        coffees: [
          {
            id: 1,
            img: 'https://www.seriouseats.com/thmb/x5dQAByuE9saNvybQ4sjTU1dHG8=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/20230621-SEA-DalognaCoffee-LorenaMasso-hero-e6a0eb179a2d457fb40c059d91594c35.jpg',
            title: 'Dalgona Coffee',
            rating: '4',
            desc: 'Dalgona Coffee is a beverage originating from Macau made by whipping equal parts instant coffee powder, sugar, and hot water until it becomes creamy and then adding it to cold or hot milk.',
            category: [
              { 
                id: 1,
                name: "Diagram"
              },
              { 
                id: 2,
                name: "Use Case"
              }
            ]
          },  
          {
            id: 2,
            img: 'https://i.insider.com/610c373d2a24d0001861ede4?width=1136&format=jpeg',
            title: 'Nigga Coffee',
            rating: '4.5',
            desc: 'Nigga Coffee offering bold, high-quality brews with a lighthearted twist. Perfect for those who enjoy their coffee with a side of laughter!',
            category: [
              { 
                id: 1,
                name: "Website"
              },
              { 
                id: 2,
                name: "Landing Page"
              }
            ]
          },
          {
            id: 3,
            img: 'https://cdn.loveandlemons.com/wp-content/uploads/2023/06/iced-matcha-latte.jpg',
            title: 'Matcha Latte',
            rating: '4.5',
            desc: 'MatchaLatte is a fun parody of classic matcha drinks, blending earthy flavors with humor. Enjoy a delicious, high-quality latte experience with a playful twist for matcha lovers!',
            category: [
              { 
                id: 1,
                name: "3D Model"
              },
              { 
                id: 2,
                name: "Animation"
              }
            ]
          },
          {
            id: 4,
            img: 'https://www.healthyfood.com/wp-content/uploads/2016/11/Dark-hot-chocolate-1.jpg',
            title: 'Nigga Chocolate',
            rating: '3.5',
            desc: 'Nigga Chocolate is a playful take on dark chocolate, blending rich, bold flavors with a touch of humor. Perfect for those who enjoy deep, intense chocolate with a fun, lighthearted twist!',
            category: [
              { 
                id: 1,
                name: "3D Model"
              },
              { 
                id: 2,
                name: "Animation"
              }
            ]
          },
        ]
      }
  },
  methods: {
    PushToOurMenus() {
      this.$router.push('/projects')
    },
    checkScreenSize() {
      this.isMobile = window.innerWidth <= 600;
    },
  },
  mounted() {
    this.checkScreenSize();
    window.addEventListener('resize', this.checkScreenSize);
  }

}
</script>

<template>
  <ToolbarComp>
    <v-container fluid>
      <v-row class="about-us">
        <v-col cols="12" md="6">
          <v-img
            cover
            :height="isMobile ? 350 : 800"
            src="https://i.postimg.cc/pdcsSThS/rescale.png"
            class="fade-img"
          >
          <div class="fade-overlay"></div>
        </v-img>
        </v-col>
        <v-col cols="12" md="6" class="align-self-center">
          <v-row class="titlesm-row" >
            <a class="fw-semibold text-dark"> Web Developer | Fullstack Developer </a>
          </v-row>
          <v-row class="title-row" >
            <a class="fw-bolder text-dark lh-1"> Farrel Ahmad Darmawan </a>
          </v-row>
          <v-row class="content-row">
            <p class="lh-base">
              I am a graduate of Telkom University Surabaya, Software Engineering program. I have experience and expertise in developing applications using technologies such as Laravel, Vue.js, AdonisJS, and managing databases like PostgreSQL and MySQL. I excel in creating efficient and scalable web-based solutions.
            </p>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <v-container fluid>
      <v-row class="mt-5 about-us">
        <v-col class="align-self-center my-education">
          <v-row class="subtitle-row" >
            <a style="font-weight: 600;"> &mdash; Tentang Saya </a>
          </v-row>
          <v-row class="title-row" >
            <a style="font-weight: 800;">My Education </a>
          </v-row>
        </v-col>
        <v-col class="align-self-center">
          <v-row class="content-row">
            <v-timeline align="start" side="end">
              <v-timeline-item
                dot-color="pink"
                size="small"
              >
                <div class="d-flex">
                  <strong class="me-4">2014</strong>
                  <div>
                    <strong>SDIT At-Taqwa</strong>
                    <div class="text-caption">
                      Sekolah Dasar
                    </div>
                  </div>
                </div>
              </v-timeline-item>

              <v-timeline-item
                dot-color="teal-lighten-3"
                size="small"
              >
                <div class="d-flex">
                  <strong class="me-4">2017</strong>
                  <div>
                    <strong>SMP Negeri 1 Surabaya</strong>
                    <div class="text-caption mb-2">
                      Junior Highscool
                    </div>
                  </div>
                </div>
              </v-timeline-item>

              <v-timeline-item
                dot-color="pink"
                size="small"
              >
                <div class="d-flex">
                  <strong class="me-4">2020</strong>
                  <div>
                    <strong>SMA Negeri 2 Surabaya</strong>
                    <div class="text-caption mb-2">
                      Senior Highschool
                    </div>
                  </div>
                </div>
              </v-timeline-item>

              <v-timeline-item
                dot-color="teal-lighten-3"
                size="small"
              >
                <div class="d-flex">
                  <strong class="me-4">2024</strong>
                  <div>
                    <strong>Telkom University Surabaya</strong>
                    <div class="text-caption mb-2">
                      University
                    </div>
                  </div>
                </div>
              </v-timeline-item>
            </v-timeline>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <v-container fluid>
      <v-row class="mt-5 about-us">
        <v-col cols="12" md="6" class="align-self-center my-education">
          <v-row class="subtitle-row" >
            <a style="font-weight: 800;"> &mdash; Tentang Saya </a>
          </v-row>
          <v-row class="title-row" >
            <a style="font-weight: 800;"> My Tech Stack </a>
          </v-row>
        </v-col>
        <v-col cols="12" md="6" class="align-self-center">
          <v-row class="content-row">
            <v-col 
              v-for="item in tech.slice(0, 5)" 
              :key="item.id" 
              class="text-center"
            >
              <v-icon 
                :icon="item.icon" 
                :color="item.color" 
                :size="isMobile ? 60 : 80">
              </v-icon>
              <p style="font-weight: bold; font-size: 12px;">{{ item.title }}</p>
            </v-col>
          </v-row>
          <v-row class="content-row">
            <v-col 
              v-for="item in tech.slice(5)" 
              :key="item.id" 
              class="text-center"
            >
              <v-icon 
                :icon="item.icon" 
                :color="item.color" 
                :size="isMobile ? 60 : 80">
              </v-icon>
              <p style="font-weight: bold; font-size: 12px;">{{ item.title }}</p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <v-container fluid style="background-color: #EEEEEE">
        <v-row class="service" 
        >
          <v-col cols="12">
            <v-card
              class="mx-auto p-5"
              style="border-radius: 24px;"
            >
            <v-row>
              <v-col align-self="center" >
                <v-row justify="center">
                  <v-avatar
                   :size="isMobile ? 200 : 450"
                  >
                    <v-img
                      alt="Ava"
                      src="https://wallpapercave.com/wp/wp7926787.jpg"
                    ></v-img>
                  </v-avatar>
                </v-row>
                <v-row justify="center">
                  <a class="title-profile"> Mr. Riz Xtar</a>
                </v-row>
              </v-col>
              <v-col class="align-self-center">
                <v-row class="text-owner">
                  <p>
                    "Terima kasih sudah datang ke kafe saya dan membuat saya makin kaya. Kalian beli kopi, saya dapat untung! Semoga uang kalian cukup untuk balik lagi besok. Jangan lupa ajak teman, biar saya makin sukses."
                  </p>
                </v-row>
              </v-col>
            </v-row>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
      <v-container fluid >
        <v-row class="projects">
          <v-col>
            <v-row>
              <v-col>
                <a class="project-header"> My Projects </a>
              </v-col>
              <v-col class="text-end align-end me-5">
                <a @click="PushToOurMenus" style="font-size: 15px; font-weight: 200; cursor: pointer"> See More <v-icon icon="mdi-arrow-right-thin" size="small"></v-icon> </a>
              </v-col>
            </v-row>
            <v-row class="pt-7">
              <v-col cols="12" sm="3" v-for="(item, index) in coffees"
              :key="index">
                <v-card
                  class="mx-auto mb-2"
                  max-width="378"
                  min-height="500"
                  style="display: flex; flex-direction: column; border-radius: 12px;"
                >
                  <v-img
                    class="align-end text-white"
                    :src="item.img"
                    aspect-ratio="1/1"
                    max-height="300"
                    cover
                  >
                  </v-img>
                  <v-card-title class="px-2">
                    <v-rating
                      hover
                      :length="5"
                      :size="32"
                      :model-value="item.rating"
                      active-color="primary"
                      half-increments
                      readonly
                    />

                    <p style="font-weight: 700; color: #967259;">Rp. 20.000</p>
                  </v-card-title>
                  <v-card-text>
                    <a class="text-h5 text-dark font-weight-black p-2"> {{ item.title }}</a>
                  </v-card-text>
                  <v-card-text class="px-2 mb-2">
                    <p >{{ item.desc }}</p>
                  </v-card-text>
                </v-card>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </ToolbarComp>
    <FooterComp />
</template>

<style scoped>
* {
  padding: 0;
  margin: 0;
  font-family: 'Poppins';
  text-decoration: none;
  list-style: none;
}

.fade-img {
  position: relative;
}

.fade-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to right, rgba(255, 255, 255, 0) 60%, rgba(255, 255, 255, 1) 95%, rgba(255, 255, 255, 1) 100%);
}


.titlesm-row {
  font-size: 24px;
}
.title-row {
  font-size: 64px;
}

.subtitle-row {
  font-size: 24px;
}

.text-content h3 {
  font-size: 2rem; 
  margin: 0;
}



.text-content p {
  font-size: 1rem; 
  margin: 0;
}

.about-us {
  padding-top: 60px;
  margin-bottom: 80px;
}

.my-education {
  padding-left: 80px;
}

.content-row {
  padding-top: 0;
  padding-right: 80px;
  font-size: 20px;
}

.content-owner {
  padding-right: 80px;
  font-size: 24px;
}

.service {
  padding-left: 130px;
  padding-right: 130px;
  padding-top: 100px;
  padding-bottom: 100px;
}

.title-profile {
  font-size: 32px;
  color: #080808;  
}

.text-owner {
  font-size: 32px;
  color: #080808;
}

.service-paragraph{
  padding-top: 30px;
}

.projects {
  padding-left: 130px;
  padding-right: 130px;
  padding-top: 80px;
  margin-bottom: 80px;
}

.project-header {
  font-size: 36px; 
  font-weight: 600;
  color: #212529
}


@media (max-width: 600px) {

  [data-aos] {
    opacity: 1 !important;
    transform: none !important;
    transition: none !important;
  }
  .fade-img {
    position: relative;
  }
  .fade-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 200px;
    background: linear-gradient(to right, rgba(255, 255, 255, 0) 100%, rgba(255, 255, 255, 1) 95%, rgba(255, 255, 255, 1) 100%);
  }

  .titlesm-row {
    font-size: 20px;
    margin-top: 20px;
    padding-left: 10px;
    padding-right: 10px;
  }
  .title-row {
    font-size: 32px;
    padding-left: 10px;
    padding-right: 10px;
  }

  .title-profile {
    font-size: 24px;
    color: #080808;  
  }
  .text-owner {
  font-size: 22px;
  color: #080808;
}
  .carousel-block {
    width: 100%;
    height: 100%;
    max-height: 150px;
    margin-top: 10px
  }

  .carousel-item {
    position: relative;
    height: 300px;
  }

  .transparent-sheet {
    background-color: transparent !important;
    box-shadow: none;
    height: 20%;
  }

  .text-content h3 {
    padding-top: 40px;
    font-size: 1.15rem;
  }
  .text-content p {
    font-size: 0.575rem;
  }

  .about-us {
    padding-left: 10px;
    padding-right: 10px;
  }
  .content-row {
    padding-top: 20px;
    padding-left: 10px;
    padding-right: 10px;
  }

  .my-education {
    padding-left: 10px;
  }   

  .service {
    padding-left: 10px;
    padding-right: 10px;
  }

  .projects {
    padding-left: 10px;
    padding-right: 10px;
  }

  .project-header {
    font-size: 24px; 
    font-weight: 600;
    color: #212529
  }
}

</style>