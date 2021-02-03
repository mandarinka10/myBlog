<template>
  <div>
    <ul class="posts">
      <li v-for="(p, i) in post" :key="i">
        <div class="row post">
          <div class="col m4 offset-m4 s10 offset-s1">
            <div class="card z-depth-2 blue-grey lighten-1 white-text">
              <div class="card-image">
                <img class="materialboxed" :src="p.imgSrc" />
              </div>
              <div class="card-content">
                <span class="card-title activator white-text"
                  ><i class="material-icons right">more_vert</i></span
                >
                <p class="text">{{ p.text }}</p>
              </div>
              <div class="card-action blue-grey darken-1" style="height: 50px">
                <span class="autor col s6">{{ p.autor }}</span>
                <span class="date right-align col s6">{{ getDate }}</span>
              </div>
              <div class="card-reveal">
                <p class="card-title grey-text text-darken-4">
                  <i class="material-icons right">close</i>Здесь скоро появятся
                  кнопочеи Редактировать Удалить мейби еще что-нибудь
                </p>
                <!-- <p class="text-darken-4">Здесь скоро появятся кнопочеи Редактировать Удалить мейби еще что-нибудь</p> -->
              </div>
            </div>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Post',
  data () {
    return {
      post: [
        {
          id: 1,
          imgSrc: require('@/assets/header-log.jpg'),
          text: 'Друзья! Добро пожаловать в мой блог!',
          autor: 'Milash'
        },
        {
          id: 2,
          imgSrc: require('@/assets/bg-home.jpg'),
          text: 'Посмотрите какая красота!',
          autor: 'Milash'
        }
      ]
    }
  },
  computed: {
    getDate () {
      let today = new Date()
      const dd = String(today.getDate()).padStart(2, '0')
      const mm = String(today.getMonth() + 1).padStart(2, '0')
      const yy = today.getFullYear()
      today = mm + '.' + dd + '.' + yy
      return today
    }
  }
}
</script>

<style scoped>

</style>
