<template>
  <div>
    <div id="card">
      <b-card no-body class="overflow-hidden" style="max-width: 1000px;">
        <b-card-text class="text-center">
          <h3 class="pt-5">My University</h3>
        </b-card-text>
        <hr>
        <b-card-img id="image" :src="require('assets/stdnt.png')" class="rounded-0"></b-card-img>
        <hr>
        <b-card-text class="text-center">
          <h1>Hi {{username}}</h1>
          <h3>Welcome to Dashboard!</h3>
        </b-card-text>
        <hr>
      </b-card>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import "assets/style.scss";
#card {
  margin-left: $margin-left !important;
  margin-top: $margin-top !important;
}

#image {
  width: $dashwidth !important;
  height: $dashheight !important;
}
</style>

<script>
export default {
  name: "card",
  data() {
    return {
      username: sessionStorage.getItem("Username")
    };
  }
};
</script>