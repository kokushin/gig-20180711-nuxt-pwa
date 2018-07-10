<template>
  <ul>
    <li v-for="item in items" :key="item.id">
      <figure>
        <img :src="item.img_src" :alt="item.name">
      </figure>
      <div class="name">{{ item.name }}</div>
      <div class="type">{{ item.type }}</div>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'CharacterList',
  data () {
    return {
      items: [
        {
          id: 1,
          name: 'もぐお',
          type: 'ノーマルタイプ',
          img_src: '/gig-20180711-nuxt-pwa/img/01.png'
        },
        {
          id: 2,
          name: '鬼もぐお',
          type: 'あくタイプ',
          img_src: '/gig-20180711-nuxt-pwa/img/02.png'
        },
        {
          id: 3,
          name: '天使もぐお',
          type: 'ひこうタイプ',
          img_src: '/gig-20180711-nuxt-pwa/img/03.png'
        },
        {
          id: 4,
          name: '究極完全体もぐお',
          type: 'かみタイプ',
          img_src: '/gig-20180711-nuxt-pwa/img/04.png'
        }
      ]
    }
  }
}
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

li {
  background-color: #fff;
  padding: 1rem;
  max-width: 400px;
  box-shadow: 0 0 4px rgba(0,0,0,.16);
  border-radius: 4px;
}

li + li {
  margin-top: 1.5rem;
}

figure img {
  width: 100%;
  height: auto;
}

.name {
  font-size: 1.5rem;
  font-weight: bold;
  margin-top: .5rem;
}
</style>
