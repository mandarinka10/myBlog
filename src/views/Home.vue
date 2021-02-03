<template>
  <div class="home blue-grey darken-3">
    <div class="addPostbtn">
      <a href="addPost" class="btn-floating btn-large waves-effect waves-light blue-grey darken-1"><i class="material-icons">add</i></a>
    </div>
    <Post />
     <!-- Modal Trigger -->
   <button data-target="modal1" class="btn modal-trigger">Modal</button>

  <!-- Modal Structure -->
  <div id="modal1" class="modal">
    <div class="modal-content">
      <h4>Modal Header</h4>
      <p>A bunch of text</p>
    </div>
    <div class="modal-footer">
      <a href="#!" class="modal-close waves-effect waves-green btn-flat">Agree</a>
    </div>
  </div>
  </div>
</template>

<script>
import Post from '../components/Post.vue'
export default {
  components: { Post },
  name: 'Home',
  data () {
    return {
      inputValue: '',
      notes: []
    }
  },
  methods: {}
  // components: {
  // addPost
  // }
}
</script>

<style scoped>
.home {
  font-family: "Neucha";
  text-align: center;
}
.addPostbtn{
  padding-top: 22px;
}
</style>
