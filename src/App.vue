<template>
    <div class="charsheet">
      <div class="modalContainer" v-if="showModal" >
        <SettingsModal @close="toggleModal" @save="saveCharacter" @load="loadCharacter"/>
      </div>
      <div>
        <div class="strdexwil">
          <input type="text" class="statbox" id="strCur" :value=strCur>
          <input type="text" class="statbox" id="strMax" :value=strMax style="margin-right: 33px;">
          <input type="text" class="statbox" id="dexCur" :value=dexCur>
          <input type="text" class="statbox" id="dexMax" :value=dexMax style="margin-right: 35px;">
          <input type="text" class="statbox" id="wilCur" :value=wilCur>
          <input type="text" class="statbox" id="wilMax" :value=wilMax>
        </div>
    </div>
    <div>
      <div class="armorhp">
        <input type="text" class="statbox" id="armor" :value=armor style="margin-right: 51px;">
        <input type="text" class="statbox" id="hpCur" :value=hpCur>
        <input type="text" class="statbox" id="hpMax" :value=hpMax>
      </div>
      <div class="deprived">
        <input type="text" class="statbox" id="deprived" :value=deprived>
      </div>
    </div>
    <div>
      <div class="coins">
        <input type="text" class="statbox" id="gold" :value=gold style="height: 21px; width: 21px;">
        <input type="text" class="statbox" id="silver" :value=silver style="height: 21px; width: 21px;">
        <input type="text" class="statbox" id="copper" :value=copper style="height: 21px; width: 21px;">
      </div>
    </div>
    <div>
      <div class="notes">
        <textarea class="notebox" id="notes" :value=notes></textarea>
      </div>
    </div>
    <div>
      <div class="pack">
        <div class="hand">
          <input type="checkbox" class="smallbox" id="hand1" >
          <input type="checkbox" class="smallbox" id="hand2" >
          <input type="checkbox" class="smallbox" id="hand3" >
          <input type="checkbox" class="smallbox" id="hand4" >
          <input type="checkbox" class="smallbox" id="hand5" >
          <input type="checkbox" class="smallbox" id="hand6" >
          <input type="checkbox" class="smallbox" id="hand7" >
          <input type="checkbox" class="smallbox" id="hand8" >
          <input type="checkbox" class="smallbox" id="hand9" >
          <input type="checkbox" class="smallbox" id="hand10">
          <!-- <input type="text" class="smallbox" id="hand1" :value=hand1>
          <input type="text" class="smallbox" id="hand2" :value=hand2>
          <input type="text" class="smallbox" id="hand3" :value=hand3>
          <input type="text" class="smallbox" id="hand4" :value=hand4>
          <input type="text" class="smallbox" id="hand5" :value=hand5>
          <input type="text" class="smallbox" id="hand6" :value=hand6>
          <input type="text" class="smallbox" id="hand7" :value=hand7>
          <input type="text" class="smallbox" id="hand8" :value=hand8>
          <input type="text" class="smallbox" id="hand9" :value=hand9>
          <input type="text" class="smallbox" id="hand10" :value=hand10> -->
        </div>
        <div class="item">
          <input type="text" class="itembox" id="item1" :value=item1>
          <input type="text" class="itembox" id="item2" :value=item2>
          <input type="text" class="itembox" id="item3" :value=item3>
          <input type="text" class="itembox" id="item4" :value=item4>
          <input type="text" class="itembox" id="item5" :value=item5>
          <input type="text" class="itembox" id="item6" :value=item6>
          <input type="text" class="itembox" id="item7" :value=item7>
          <input type="text" class="itembox" id="item8" :value=item8>
          <input type="text" class="itembox" id="item9" :value=item9>
          <input type="text" class="itembox" id="item10" :value=item10>
        </div>
        <div class="fatigue">
          <input type="text" class="smallboxfatigue" id="fatigue1" :value=fatigue1>
          <input type="text" class="smallboxfatigue" id="fatigue2" :value=fatigue2>
          <input type="text" class="smallboxfatigue" id="fatigue3" :value=fatigue3>
          <input type="text" class="smallboxfatigue" id="fatigue4" :value=fatigue4>
          <input type="text" class="smallboxfatigue" id="fatigue5" :value=fatigue5>
          <input type="text" class="smallboxfatigue" id="fatigue6" :value=fatigue6>
          <input type="text" class="smallboxfatigue" id="fatigue7" :value=fatigue7>
          <input type="text" class="smallboxfatigue" id="fatigue8" :value=fatigue8>
          <input type="text" class="smallboxfatigue" id="fatigue9" :value=fatigue9>
          <input type="text" class="smallboxfatigue" id="fatigue10" :value=fatigue10>
        </div>
      </div>
    </div>
    <div>
        <div class="name">
          <input type="text" class="namebox" id="charname" :value=charname>
        </div>
    </div>
    <div>
        <div class="menu">
          <div class="menubox" @click="toggleModal"></div>
        </div>
    </div>


    </div>
    
</template>

<script>

import SettingsModal from './components/SettingsModal.vue'
import { NButton } from 'naive-ui'

export default {
  name: 'App',
  components: { SettingsModal },
  data() {
    return {
      showModal: false,
      strCur: null,
      strMax: null,
      dexCur: null,
      dexMax: null,
      wilCur: null,
      wilMax: null,
      armor: null,
      hpCur: null,
      hpMax: null,
      gold: null,
      silver: null,
      copper: null,
      notes: null,
      hand1: null,
      hand2: null,
      hand3: null,
      hand4: null,
      hand5: null,
      hand6: null,
      hand7: null,
      hand8: null,
      hand9: null,
      hand10: null,
      item1: null,
      item2: null,
      item3: null,
      item4: null,
      item5: null,
      item6: null,
      item7: null,
      item8: null,
      item9: null,
      item10: null,
      fatigue1: null,
      fatigue2: null,
      fatigue3: null,
      fatigue4: null,
      fatigue5: null,
      fatigue6: null,
      fatigue7: null,
      fatigue8: null,
      fatigue9: null,
      fatigue10: null,
      charname: null
  }
},
  methods: {
    toggleModal() {
      this.setStats()
      this.showModal = !this.showModal;
    },
    setStats() {
      this.strCur = document.getElementById("strCur").value
      this.strMax = document.getElementById("strMax").value
      this.dexCur = document.getElementById("dexCur").value
      this.dexMax = document.getElementById("dexMax").value
      this.wilCur = document.getElementById("wilCur").value
      this.wilMax = document.getElementById("wilMax").value
      this.armor = document.getElementById("armor").value
      this.hpCur = document.getElementById("hpCur").value
      this.hpMax = document.getElementById("hpMax").value
      this.deprived = document.getElementById("deprived").value
      this.gold = document.getElementById("gold").value
      this.silver = document.getElementById("silver").value
      this.copper = document.getElementById("copper").value
      this.notes = document.getElementById("notes").value
      this.hand1 = document.getElementById("hand1").value
      this.hand2 = document.getElementById("hand2").value
      this.hand3 = document.getElementById("hand3").value
      this.hand4 = document.getElementById("hand4").value
      this.hand5 = document.getElementById("hand5").value
      this.hand6 = document.getElementById("hand6").value
      this.hand7 = document.getElementById("hand7").value
      this.hand8 = document.getElementById("hand8").value
      this.hand9 = document.getElementById("hand9").value
      this.hand10 = document.getElementById("hand10").value
      this.item1 = document.getElementById("item1").value
      this.item2 = document.getElementById("item2").value
      this.item3 = document.getElementById("item3").value
      this.item4 = document.getElementById("item4").value
      this.item5 = document.getElementById("item5").value
      this.item6 = document.getElementById("item6").value
      this.item7 = document.getElementById("item7").value
      this.item8 = document.getElementById("item8").value
      this.item9 = document.getElementById("item9").value
      this.item10 = document.getElementById("item10").value
      this.fatigue1 = document.getElementById("fatigue1").value
      this.fatigue2 = document.getElementById("fatigue2").value
      this.fatigue3 = document.getElementById("fatigue3").value
      this.fatigue4 = document.getElementById("fatigue4").value
      this.fatigue5 = document.getElementById("fatigue5").value
      this.fatigue6 = document.getElementById("fatigue6").value
      this.fatigue7 = document.getElementById("fatigue7").value
      this.fatigue8 = document.getElementById("fatigue8").value
      this.fatigue9 = document.getElementById("fatigue9").value
      this.fatigue10 = document.getElementById("fatigue10").value
      this.charname = document.getElementById("charname").value
    },
    saveCharacter() {
      // let strCur, strMax, dexCur, dexMax, wilCur, wilMax, armor, hpCur, hpMax, deprived, gold, silver, copper, notes, hand1, hand2, hand3, hand4, hand5, hand6, hand7, hand8, hand9, hand10, item1, item2, item3, item4, item5, item6, item7, item8, item9, item10, fatigue1, fatigue2, fatigue3, fatigue4, fatigue5, fatigue6, fatigue7, fatigue8, fatigue9, fatigue10, name
      this.setStats()
      let CharacterOne = {
        Charname: this.charname,
        Str: {
          current: this.strCur,
          max: this.strMax,
        },
        Dex: {
          current: this.dexCur,
          max: this.dexMax,
        },
        Wil: {
          current: this.wilCur,
          max: this.wilMax,
        },
        Armor: this.armor,
        HP: {
          current: this.hpCur,
          max: this.hpMax,
        },
        Money: {
          gold: this.gold,
          silver: this.silver,
          copper: this.copper
        },
        Deprived: this.deprived,
        Notes: this.notes,
        Pack: {
          ItemOne: this.item1,
          ItemTwo: this.item2,
          ItemThree: this.item3,
          ItemFour: this.item4,
          ItemFive: this.item5,
          ItemSix: this.item6,
          ItemSeven: this.item7,
          ItemEight: this.item8,
          ItemNine: this.item9,
          ItemTen: this.item10,
        },
        Hand: {
          ItemOne: this.hand1,
          ItemTwo: this.hand2,
          ItemThree: this.hand3,
          ItemFour: this.hand4,
          ItemFive: this.hand5,
          ItemSix: this.hand6,
          ItemSeven: this.hand7,
          ItemEight: this.hand8,
          ItemNine: this.hand9,
          ItemTen: this.hand10,
        },
        Fatigue: {
          ItemOne: this.fatigue1,
          ItemTwo: this.fatigue2,
          ItemThree: this.fatigue3,
          ItemFour: this.fatigue4,
          ItemFive: this.fatigue5,
          ItemSix: this.fatigue6,
          ItemSeven: this.fatigue7,
          ItemEight: this.fatigue8,
          ItemNine: this.fatigue9,
          ItemTen: this.fatigue10,
        }
    }
    localStorage.setItem("character", JSON.stringify(CharacterOne))
    this.toggleModal()
  },
  loadCharacter() {
    let char = JSON.parse(localStorage.getItem("character"))
      this.strCur = char.Str.current
      this.strMax = char.Str.max
      this.dexCur = char.Dex.current
      this.dexMax = char.Dex.max
      this.wilCur = char.Wil.current
      this.wilMax = char.Wil.max
      this.armor = char.Armor
      this.hpCur = char.HP.current
      this.hpMax = char.HP.max
      this.deprived = char.Deprived
      this.gold = char.Money.gold
      this.silver = char.Money.silver
      this.copper = char.Money.copper
      this.notes = char.Notes
      this.hand1 = char.Hand.ItemOne
      this.hand2 = char.Hand.ItemTwo
      this.hand3 = char.Hand.ItemThree
      this.hand4 = char.Hand.ItemFour
      this.hand5 = char.Hand.ItemFive
      this.hand6 = char.Hand.ItemSix
      this.hand7 = char.Hand.ItemSeven
      this.hand8 = char.Hand.ItemEight
      this.hand9 = char.Hand.ItemNine
      this.hand10 = char.Hand.ItemTen
      this.item1 = char.Pack.ItemOne
      this.item2 = char.Pack.ItemTwo
      this.item3 = char.Pack.ItemThree
      this.item4 = char.Pack.ItemFour
      this.item5 = char.Pack.ItemFive
      this.item6 = char.Pack.ItemSix
      this.item7 = char.Pack.ItemSeven
      this.item8 = char.Pack.ItemEight
      this.item9 = char.Pack.ItemNine
      this.item10 = char.Pack.ItemTen
      this.fatigue1 = char.Fatigue.ItemOne
      this.fatigue2 = char.Fatigue.ItemTwo
      this.fatigue3 = char.Fatigue.ItemThree
      this.fatigue4 = char.Fatigue.ItemFour
      this.fatigue5 = char.Fatigue.ItemFive
      this.fatigue6 = char.Fatigue.ItemSix
      this.fatigue7 = char.Fatigue.ItemSeven
      this.fatigue8 = char.Fatigue.ItemEight
      this.fatigue9 = char.Fatigue.ItemNine
      this.fatigue10 = char.Fatigue.ItemTen
      this.charname = char.Charname
      this.showModal = !this.showModal;
  }
}
}
</script>

<style>
:root {
  --grey: #B7B7B7;
}

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
  margin-top: -242px;
  margin-left: 49px;
 }
 /* .pack{
  display: flex;
  margin-top: -240px;
  margin-left: 53px;
 } */
 .menu{
  display: flex;
  margin-top: -275px;
  margin-left: 187px;
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
height: 14px;
width: 14px;
text-align: center;
border: none;
margin-bottom: 9px;

  }

  /* .smallbox {
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
  } */

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
  height: 24px;
  width: 103px;
  border: none;
  text-align: start;
  }

  .menubox {
  background-color: transparent;
  height: 50px;
  width: 131px;
  border: none;
  text-align: start;
  }
  .menubox:hover {
    background-color: rgba(0,0,0,0.5);
    border-radius: 10px;
  }


</style>

