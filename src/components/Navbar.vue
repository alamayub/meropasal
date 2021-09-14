<template>
  <v-app-bar app color="white">
    <v-container class="d-flex align-center">
      <div class="d-flex align-center">
        <v-img alt="Vuetify Logo" class="shrink" contain src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png" transition="scale-transition" width="40" />
      </div>

      <div class="nav">
        <ul>
          <li v-for="a in 5" :key="a" class="nav__parent px-3">
            <div class="nav__parent__title">Parent</div>
            <ul class="child white px-5 py-3">
              <li v-for="b in 2" :key="b" class="nav__child">
                <div class="nav__child__title py-1">Child</div>
                <div v-for="c in 5" :key="c" class="grand__child__title my-1">Grand Child</div>
              </li>
            </ul>
          </li>
        </ul>
      </div>

      <v-spacer></v-spacer>
      <v-btn href="https://github.com/vuetifyjs/vuetify/releases/latest" target="_blank" text>
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-container>
  </v-app-bar>
</template>

<style scoped>
.nav {
  height: 64px;
  width: 100%;
}
ul { 
  padding: 0 !important;
  margin: 0 !important;
  list-style: none;
}
ul li { 
  letter-spacing: .5px;
  position: relative; 
}
.nav__parent {
  float: left; 
  height: 64px;
  transition: ease-in-out 100ms;
}
.nav__parent__title {
  cursor: pointer;
  height: 100%;
  width: 100%;
  font-weight: 500;
  text-transform: uppercase; 
  line-height: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
ul .child { 
  display: none; 
  position: absolute;
  top: 64px;
  /* left: calc(100% - 200px); */
  left: 0;
  min-width: 350px;
  box-shadow: 0 4px 10px 0 rgb(0 0 0 / 10%);
  border-radius: 1px;
}
ul .nav__parent:hover { border-bottom: 5px solid pink; }
ul > li:hover ul { 
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(48%, 1fr));
  grid-gap: 12px; 
}
ul > li > ul > li .nav__child__title {
  font-size: 15px;
  font-weight: 400;
  line-height: 1;
  cursor: pointer;
}
.grand__child__title {
  color: rgb(0 0 0 / 70%);
  font-weight: 300;
  font-size: 13px;
  cursor: pointer;
  transition: ease-in-out 100ms;
}
.grand__child__title:hover { font-weight: 500; }
</style>