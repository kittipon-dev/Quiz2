<template>
  <div>
    <v-app-bar color="#2961E2">
      <v-container>
        <v-row>
          <v-col lg="11" cols="9"><div id="name">Morning, Kevin</div></v-col>
          <v-col lg="1" cols="3">
            <div>
              <v-avatar>
                <img src="https://cdn.vuetifyjs.com/images/john.jpg" />
              </v-avatar>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-app-bar>
    <nuxt />
  </div>
</template>
<style scoped>
#name {
  padding: 15px;
  font-size: 17px;
  color: #ffffff;
  text-align: right;
}
@media screen and (max-device-width: 600px) {
  #name {
    text-align: left;
  }
}
</style>
<style>
body {
  background-color: #e5e5e5;
}
#title {
  color: #273253;
  font-family: PT Sans;
  font-style: normal;
  font-weight: bold;
  font-size: 14px;
}
#short_description {
  color: #838383;
  font-family: Prompt;
  font-style: normal;
  font-weight: 500;
  font-size: 11px;
}
</style>
