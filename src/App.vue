<template>
  <div id="app" class="noselect">
    <div class="wrapper">
      <div id="image">
        <div id="display_of_radio">
          <span>Eska</span>
        </div>
        <div class="switch_station" @click="stationClick(2)">2</div>
        <div class="switch_station" @click="stationClick(3)">3</div>
        <div class="switch_station" @click="stationClick(4)">4</div>
        <div class="switch_station" @click="stationClick(5)">5</div>
        <div class="switch_station" @click="stationClick(6)">6</div>
        <div class="switch_station" @click="stationClick(1)">1</div>
      </div>
    <div id="legend">
      <p>#1 - Eska</p>
      <p>#2 - Radio Zet</p>
      <p>#3 - RMF FM</p>
      <p>#4 - Radio Maryja</p>
      <p>#5 - Radio Bielsko</p>
      <p>#6 - Anty-Radio</p>
    </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'app',
  components: {
  },
  methods: {
    stationClick(num_station) {
      // eslint-disable-next-line
      console.log('station clicked', num_station);
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100%;
  background-color: #e0e0e0;
  flex-shrink: 0;
}

.wrapper {
  width: 100%;
  justify-content: center;
}

#image {
  background: url('https://www.caraudio-service.ru/BMW_Business-CD-RDS_BP3850_6512-8352865_7643850340_EU.jpg');
  background-repeat: no-repeat;
  background-size: 100%;
  width: 500px;
  height: 300px;
  margin: 0 auto 0 auto;
  position: relative;
}

#legend {
  width: 130px;
  margin: 35px auto 0 auto;
}

#display_of_radio {
  top: 78px;
  left: 136px;
  width: 228px;
  height: 39px;
  position: absolute;
  background-color: black;
  border-radius: 2px;
  opacity: 1.0;
  text-align: center;
}

#display_of_radio span{
  font-size: 2.0em;
  font-weight: 600;
  color: orange;
}

.switch_station {
  top: 126px;
  left: 133px;
  width: 28px;
  height: 22px;
  position: absolute;
  background-color: red;
  border-radius: 2px;
  opacity: 0;
  text-align: center;
}

.switch_station:hover {
  cursor: pointer;
}

.switch_station:nth-of-type(2) {
  left: 162px;
}

.switch_station:nth-of-type(3) {
  left: 200px;
}

.switch_station:nth-of-type(4) {
  left: 228px;
}

.switch_station:nth-of-type(5) {
  left: 265px;
}

.switch_station:nth-of-type(6) {
  left: 294px;
}









.noselect {
  -webkit-touch-callout: none; /* iOS Safari */
    -webkit-user-select: none; /* Safari */
     -khtml-user-select: none; /* Konqueror HTML */
       -moz-user-select: none; /* Firefox */
        -ms-user-select: none; /* Internet Explorer/Edge */
            user-select: none; /* Non-prefixed version, currently
                                  supported by Chrome and Opera */
}

</style>
