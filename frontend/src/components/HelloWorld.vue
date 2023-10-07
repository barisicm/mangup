<script lang="ts" setup>
import {reactive} from 'vue'
import {Greet} from '../../wailsjs/go/main/App'

const data = reactive({
  name: "",
  resultText: "Please enter your name below 👇",
})

function greet() {
  Greet(data.name).then(result => {
    data.resultText = result
  })
}

</script>

<template>
  <main class="container-fluid vh-100 p-0">
    <nav class="row row-cols-lg-auto g-3 align-items-center">
      <div class="col-12">
        <p>Test1</p>
      </div>
      <div class="col-12">
        <button class="btn btn-primary">Click me</button>
      </div>
    </nav>
    <div class="row">
      <div class="vh-100 col-1"></div>
      <div class="vh-100 col-3"></div>
      <div class="vh-100 col-7"></div>
      <div class="vh-100 col-1"></div>
    </div>
    <nav class="row">

    </nav>


    <!--    <div id="result" class="result">{{ data.resultText }}</div>
    <div id="input" class="input-box">
      <input id="name" v-model="data.name" autocomplete="off" class="input" type="text"/>
      <button class="btn" @click="greet">Greet</button>
    </div>-->
  </main>
</template>

<style scoped>

</style>
