<template>
  <div id="app" class="app">
    <main>
      <div class="search-box">
        <input class="search-bar" type="text" placeholder="Search..." />
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      api_key: "62772885f679b3cedad02112c05144cb",
    };
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  font-family: "Montserrat", sans-serif;
}

.app {
  background-image: url("./assets/images/cloud-bg.jpeg");
  background-size: cover;
  background-position: bottom;
  transition: 0.4s;
}

main {
  min-height: 100vh;
  padding: 25px;
  background-image: linear-gradient(
    to bottom,
    rgba(0, 0, 0, 0.25),
    rgba(0, 0, 0, 0.75)
  );
}

.search-box {
  width: 100%;
  margin-bottom: 30px;
}
.search-box .search-bar {
  display: block;
  width: 80%;
  margin: auto;
  padding: 13px 10px;
  font-size: 18px;
  outline: none;
  border: none;
  appearance: none;
  color: #454545;
  background-color: rgba(255, 255, 255, 0.5);
  box-shadow: 0 0 8px 1px #3a3939;
  transition: 0.3s;
}
.search-box .search-bar:focus {
  box-shadow: 0 0 16px 1px #3a3939;
}
</style>
