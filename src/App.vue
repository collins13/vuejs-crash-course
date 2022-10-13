<template>
  <h1>{{title}}</h1>
  <p>welcome!!</p>
  <teleport to='modals' v-if="showModal">
    <Modal theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href="#">signup</a>
      </template>
      <h1>signup modal for vue</h1>
      <p>half price machine swag!</p>
    </Modal>
  </teleport>
  <button @click="toggleModal">show modal</button>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
 import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components:{
    Modal
  },
  data(){
    return {
      title: "my vue application",
      showModal:false
    }
  },
  methods:{
    toggleModal(){
      this.showModal = !this.showModal
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1{
  border: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
