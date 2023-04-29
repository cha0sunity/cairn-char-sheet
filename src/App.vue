<template>
    <div class="charsheet">
      <div>
        <div class="strdexwil">
          <input type="text" class="statbox">
          <input type="text" class="statbox" style="margin-right: 33px;">
          <input type="text" class="statbox">
          <input type="text" class="statbox" style="margin-right: 35px;">
          <input type="text" class="statbox">
          <input type="text" class="statbox">
        </div>
    </div>
    <div>
      <div class="armorhp">
        <input type="text" class="statbox" style="margin-right: 51px;">
        <input type="text" class="statbox">
        <input type="text" class="statbox">
      </div>
      <div class="deprived">
        <input type="text" class="statbox">
      </div>
    </div>
    <div>
      <div class="coins">
        <input type="text" class="statbox" style="height: 21px; width: 21px;">
        <input type="text" class="statbox" style="height: 21px; width: 21px;">
        <input type="text" class="statbox" style="height: 21px; width: 21px;">
      </div>
    </div>
    <div>
      <div class="notes">
        <textarea class="notebox"></textarea>
      </div>
    </div>
    <div>
      <div class="pack">
        <div class="hand">
          <input type="text" class="smallbox">
          <input type="text" class="smallbox">
          <input type="text" class="smallbox">
          <input type="text" class="smallbox">
          <input type="text" class="smallbox">
          <input type="text" class="smallbox">
          <input type="text" class="smallbox">
          <input type="text" class="smallbox">
          <input type="text" class="smallbox">
          <input type="text" class="smallbox">
        </div>
        <div class="item">
          <input type="text" class="itembox">
          <input type="text" class="itembox">
          <input type="text" class="itembox">
          <input type="text" class="itembox">
          <input type="text" class="itembox">
          <input type="text" class="itembox">
          <input type="text" class="itembox">
          <input type="text" class="itembox">
          <input type="text" class="itembox">
          <input type="text" class="itembox">
        </div>
        <div class="fatigue">
          <input type="text" class="smallboxfatigue">
          <input type="text" class="smallboxfatigue">
          <input type="text" class="smallboxfatigue">
          <input type="text" class="smallboxfatigue">
          <input type="text" class="smallboxfatigue">
          <input type="text" class="smallboxfatigue">
          <input type="text" class="smallboxfatigue">
          <input type="text" class="smallboxfatigue">
          <input type="text" class="smallboxfatigue">
          <input type="text" class="smallboxfatigue">
        </div>
      </div>
    </div>
    <div>
        <div class="name">
          <input type="text" class="namebox">
        </div>
    </div>


    </div>

</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
  }
}
</script>

<style>
 .name{
  display: flex;
  margin-top: -486px;
  margin-left: 52px;
 }
 .strdexwil{
  display: flex;
  margin-top: 230px;
  margin-left: 206px;
 }
 .armorhp{
  display: flex;
  margin-top: 132px;
  margin-left: 223px;
 }
 .deprived{
  display: flex;
  margin-top: -45px;
  margin-left: 414px;
 }
 .notes{
  display: flex;
  margin-top: 84px;
  margin-left: 302px;
 }
 .coins{
  display: flex;
  margin-top: -83px;
  margin-left: 144px;
  flex-direction: column;
 }
 .pack{
  display: flex;
  margin-top: -240px;
  margin-left: 53px;
 }
 .hand {
  
 }
 .item {

 }

  .charsheet {
  /* background-color: black; */
  background-image: url("./assets/Capture.PNG");
  height: 800px;
  width: 500px;
  position: fixed;
  }

  .statbox {
  background-color: transparent;
  height: 26px;
  width: 28px;
  text-align: center;
  padding-top: 2px;
  border: none;
  }

  .itembox {
  display: flex;
  flex-direction: column;
  background-color: transparent;
  height: 20px;
  width: 157px;
  text-align: center;
  padding-top: 2px;
  border: none;
  }

  .smallbox {
  display: flex;
  flex-direction: column;
  background-color: transparent;
  height: 8px;
  width: 8px;
  text-align: center;
  padding-top: 2px;
  border: none;
  margin-bottom: 12px;
  margin-right: 1px;

  }
  .smallboxfatigue {
  display: flex;
  flex-direction: column;
  background-color: transparent;
  height: 8px;
  width: 8px;
  text-align: center;
  padding-top: 2px;
  border: none;
  margin-bottom: 12px;
  margin-left: 1px;
  margin-top: 1px;
  }

  .notebox {
  background-color: transparent;
  height: 289px;
  width: 166px;
  border: none;
  text-align: start;
  resize: none;
  }

  .namebox {
  background-color: transparent;
  height: 26px;
  width: 100px;
  border: none;
  text-align: start;
  }


</style>
