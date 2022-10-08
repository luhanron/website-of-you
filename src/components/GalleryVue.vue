<template>
  <v-container>
    <div class="block galleryBlock">
      <v-row>
        <v-col
          v-for="item in items"
          :key="item.id"
          class="d-flex child-flex"
          cols="4"
        >
          <v-hover
          v-slot="{ hover }"
          open-delay="150"
          >
            <v-card
                :elevation="hover ? 12 : 2"
                :class="{ 'on-hover': hover }"
            >
              <v-img
                :src="item.src"
                aspect-ratio="1"
                class="grey lighten-2"
              >
          <v-fade-transition>
          <v-overlay
            v-if="hover"
            absolute
            color="rgba(125, 144, 157, 1.0)"
            >
            <v-card-title>
              <p 
              :class="{ 'show-card-title': hover }"
              :color="black">
              {{ item.title }}
              </p>
              <div>
              <p class="ma-0 text-body-1 font-weight-bold font-italic text-left">
              {{ item.text }}
              </p>
              <p class="text-caption font-weight-medium font-italic text-left">
              {{ item.subtext }}
              </p>
              </div>
            </v-card-title>
          </v-overlay>
        </v-fade-transition>
                  <template v-slot:placeholder>
                  <v-row
                    class="fill-height ma-0"
                    align="center"
                    justify="center"
                  >
                    <v-progress-circular
                      indeterminate
                      color="grey lighten-5"
                    ></v-progress-circular>
                  </v-row>
                </template>
              </v-img>
            </v-card>
          </v-hover>
        </v-col>
      </v-row>
    </div>
  </v-container>
</template>

<script>
  export default {
    name: 'GalleryVue',
    data() {
    return {
      items: [
        {
          id: 1,
          title: 'Project 1',
          src: require("../assets/images/01.jpg"),
          srchover: require("../assets/images/03.jpg"),
        },
        {
          id: 2,
          title: 'Project 2',
          src: require("../assets/images/02.jpg")
        },
        {
          id: 3,
          title: 'Project 3',
          src: require("../assets/images/03.jpg")
        },
        {
          id: 4,
          title: 'Project 4',
          src: require("../assets/images/04.jpg")
        },
        {
          id: 5,
          title: 'Project 5',
          src: require("../assets/images/05.jpg")
        },
        {
          id: 6,
          title: 'Project 6',
          src: require("../assets/images/06.jpg")
        },
        {
          id: 7,
          title: 'Project 7',
          src: require("../assets/images/07.jpg")
        },
        {
          id: 8,
          title: 'Project 8',
          src: require("../assets/images/08.jpg")
        },
        {
          id: 9,
          title: 'Project 9',
          src: require("../assets/images/09.jpg")
        }
      ]
    };
    }
  };
</script>
