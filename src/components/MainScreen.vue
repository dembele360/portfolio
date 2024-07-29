<template>
  <v-container :style="{ 'background-image': `url(${require('../assets/bk.jpg')})` }">
    <v-row>
      <v-col>
        <div class="w-100 w-md-50 text-center">
          <h1 class="text-h4 text-md-h2 font-weight-bold my-6">
            Crafting Code: A Journey Through My Software Projects
          </h1>

          <div class="text-body-1 text-medium-emphasis mb-10">
            Welcome to my portfolio! Here, I highlight my most exciting and innovative software projects. As a
            passionate developer, I turn complex problems into functional code, continually evolving my skills. Explore
            how I transform ideas into impactful solutions and craft software that drives results.
          </div>

          <div class="d-flex ga-4 justify-center">
            <v-btn class="text-none" color="success" flat rounded="lg">
              Get started
            </v-btn>
            <v-btn class="text-none" color="primary" flat rounded="lg" append-icon="mdi-chevron-right">
              Learn more <v-icon title="View on Github">mdi-chevron-right</v-icon>
            </v-btn>
          </div>
        </div>

        <div class="v-bg position-absolute top-0 right-0 left-0 bottom-0">
          <div aria-hidden="true" class="overflow-hidden opacity-20 w-100 h-100" />
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'MainScreen',

  data: () => ({
    //
  }),
}
</script>
