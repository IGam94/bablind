<template lang="">
  <div>
    <div class="scene">
      <div class="cube">
        <div class="cube__face cube__face--front">{{ this.food[0] }}</div>
        <div class="cube__face cube__face--back">{{ this.food[1] }}</div>
        <div class="cube__face cube__face--right">{{ this.food[2] }}</div>
        <div class="cube__face cube__face--left">{{ this.food[3] }}</div>
        <div class="cube__face cube__face--top">{{ this.food[4] }}</div>
        <div class="cube__face cube__face--bottom">{{ this.food[5] }}</div>
      </div>
      <button class="dice" v-on:click="this.changeSide">주사위 돌리기!!</button>
    </div>
    <p class="radio-group">
      <label>
        <input type="radio" name="rotate-cube-side" value="front" />
        front
      </label>
      <label>
        <input type="radio" name="rotate-cube-side" value="right" /> right
      </label>
      <label>
        <input type="radio" name="rotate-cube-side" value="back" /> back
      </label>
      <label>
        <input type="radio" name="rotate-cube-side" value="left" /> left
      </label>
      <label>
        <input type="radio" name="rotate-cube-side" value="top" /> top
      </label>
      <label>
        <input type="radio" name="rotate-cube-side" value="bottom" /> bottom
      </label>
    </p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      food: ["이주상", "서주이", "조유진", "유순조", "윤성희", "김보경"],
      cube: "",
      radioGroup: "",
      currentClass: "",
      showClass: "",
    };
  },
  mounted() {
    this.cube = document.querySelector(".cube");
    this.radioGroup = document.querySelector(".radio-group");
    this.currentClass = "";
    this.showClass = "";
    // set initial side
  },
  methods: {
    changeSide() {
      var checkedRadio = this.radioGroup.querySelectorAll("input");

      while (
        this.currentClass == this.showClass ||
        this.showClass == undefined
      ) {
        var randomValue = Math.floor(Math.random() * 5);
        this.showClass = "show-" + checkedRadio[randomValue].value;
      }

      if (this.currentClass) {
        this.cube.classList.remove(this.currentClass);
      }
      this.cube.classList.add(this.showClass);
      this.currentClass = this.showClass;
    },
  },
};
</script>
<style lang=""></style>
