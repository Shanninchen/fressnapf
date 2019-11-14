<template>
  <v-container>
    <v-layout
      text-center
      wrap
    >
      <v-flex
        xs12
        mb-5
      >
        <h1>Images</h1>
        <p></p>
        <v-carousel
          dark
          height="600">
          <v-carousel-item
            v-for="image in images"
            :key="image"
          >
            <v-sheet
              height="800"
              tile
            >
              <v-row
                class="fill-height"
                align="center"
                justify="center"
              >
                <img :src="image" height="100%">
              </v-row>
            </v-sheet>
          </v-carousel-item>
        </v-carousel>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'Images',
  data() {
    return {
      images: [
        'image1.jpg',
        'image2.jpg',
        'image3.jpg',
        'image4.jpg',
        'image5.jpg',
      ],
    };
  },
};
</script>
