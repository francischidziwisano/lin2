<template>
  <div id="app">
    <div class="row">
    <div class="col-md-4"></div>
    <div class="col-md-4">

    <form class="form-control">
      <input class="form-control p-2 m-2" placeholder="Number 1" type="number" name="number1" v-model="number1">
      <input class="form-control p-2 m-2" placeholder="Number 2" type="number" name="number2" v-model="number2">
      <button class="form-control p-2 m-2 btn btn-primary btn-sm" @click="add()" type="button">Sum</button>
      <button class="form-control p-2 m-2 btn btn-primary btn-sm" @click="subtract()" type="button">Multiply</button>
    </form>

  </div></div>
    <div class="col-md-4"></div>
    <p>TOTAL:{{ result }}</p>
  </div>
</template>
<script>
import "bootstrap/dist/css/bootstrap.min.css"
import "bootstrap"

export default {

  data() {
    return {
      number1: 0,
      number2: 0,
      result: 0
    }
  },
  methods: {
    add() {
      this.result = parseInt(this.number1) + parseInt(this.number2);
    },
    subtract() {
      this.result = parseInt(this.number1) * parseInt(this.number2);
    }
  }
}

</script>
