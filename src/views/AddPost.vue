<template>
  <div class="addPost blue-grey darken-4">
    <div class="row">
      <form class="col m8 offset-m2 s12 blue-grey darken-1">
        <div class="row">
          <div class="input-field col s12 white-text">
            <i class="material-icons prefix">mode_edit</i>
            <textarea
              v-model="postText"
              id="icon_prefix2"
              class="materialize-textarea"
            ></textarea>
            <label class="white-text" for="icon_prefix2">Text</label>
          </div>
          <div class="input-field col s4 white-text">
            <i class="material-icons prefix">account_circle</i>
            <input
              v-model="accountName"
              id="icon_prefix"
              type="text"
              class="validate"
            />
            <label class="white-text" for="icon_prefix">Your name</label>
          </div>
          <div class="col s12">
            <button class="btn waves-effect waves-light blue-grey darken-2">
              <i class="material-icons prefix">add_a_photo</i>
            </button>
          </div>
          <div class="col s2 offset-s10">
            <button
              @click="onSubmit"
              type="button"
              class="btn waves-effect waves-light blue-grey darken-2">
              Add post
            </button>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'addPost',
  data () {
    return {
      postText: '',
      accountName: ''
    }
  },
  methods: {
    onSubmit () {
      if (this.text.trim() && this.name.trim()) {
        // const NewPost = {
        //   imgSrc: require('@/assets/header-log.jpg'),
        //   text: this.postText,
        //   name: this.accountName
        // }
        // this.$emit(addPost, NewPost)
        this.postText = ''
        this.accountName = ''
        alert('Запись добавлена')
      }
    }
  }
}
</script>

<style scoped>
.addPost {
  font-family: "Neucha";
}
</style>
