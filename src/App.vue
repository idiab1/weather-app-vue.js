<template>
  <div id="app" class="app">
    <main>
      <!-- Search Box -->
      <div class="search-box">
        <input class="search-bar" type="text" placeholder="Search..." />
      </div>
      <!-- End of Search Box -->

      <!-- Weather wrap -->
      <div class="weather-wrap">
        <div class="location-box">
          <div class="location">Cairo, Egypt</div>
          <div class="date">Monday 20 January 2020</div>
        </div>
        <div class="weather-box">
          <div class="temp">
            <h1>9°C</h1>
          </div>
          <div class="weather">
            <span>Rain</span>
          </div>
        </div>
      </div>

      <!-- End of Weather wrap -->
    </main>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      api_key: "62772885f679b3cedad02112c05144cb",
      url_base: "https://api.openweathermap.org/data/2.5/",
      query: "",
      weather: {},
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
    rgb(0 0 0 / 55%)
  );
}

.search-box {
  width: 100%;
  margin-bottom: 30px;
}
.search-box .search-bar {
  display: block;
  width: 70%;
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

/* Weather Box */

.weather-wrap {
  text-align: center;
}
.weather-wrap .location-box .location {
  font-size: 30px;
  font-weight: 500;
  color: #fff;
  text-shadow: 1px 3px rgb(0 0 0 / 25%);
}
.weather-wrap .location-box .date {
  font-weight: 300;
  color: #c9c9c9;
  font-style: italic;
  font-size: 18px;
  margin: 5px 0;
}

.weather-wrap .weather-box .temp {
  display: inline-block;
  color: #fff;
  padding: 20px 50px;
  background-color: rgba(255, 255, 255, 0.25);
  box-shadow: 3px 6px rgb(0 0 0 / 25%);
  margin: 35px 0;
  border-radius: 14px;
}

.weather-wrap .weather-box .temp h1 {
  font-weight: 900;
  font-size: 34px;
  text-shadow: 3px 6px rgb(0 0 0 / 25%);
}
.weather-wrap .weather-box .weather span {
  color: #fff;
  font-size: 21px;
  font-style: italic;
  font-weight: 700;
  text-shadow: 3px 6px rgb(0 0 0 / 25%);
}

/* End of Weather Box */
</style>
