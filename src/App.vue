<template>
  <div class="menu">
    <a v-for="(a, i) in 메뉴들" :key="i">{{i}} {{a}}</a>
  </div>
  
  <div>
    <img src="./assets/room0.jpg" class="room-img">
    <h4>{{ products[0] }}</h4>
    <p>{{ prices[0] }} 만원</p>
    <button @click="increase(0)">허위매물신고</button> <span>신고수 : {{신고수[0]}} </span>
  </div>
  <div>
    <img src="./assets/room1.jpg" class="room-img">
    <h4>{{ products[1] }}</h4>
    <p>{{ prices[1] }} 만원</p>
    <button @click="increase(1)">허위매물신고</button> <span>신고수 : {{신고수[1]}} </span>
  </div>
    <div>
      <img src="./assets/room2.jpg" class="room-img">
    <h4>{{ products[2] }}</h4>
    <p>{{ prices[2] }} 만원</p>
    <button @click="increase(2)">허위매물신고</button> <span>신고수 : {{신고수[2]}} </span>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      신고수 : [0,0,0],
      메뉴들 : ['Home', 'Shop', 'About'],
      prices : [50, 60, 70],
      스타일 : 'color : blue',
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
    }
  },

  methods : {
    increase(i){
      this.신고수[i] += 1;
    }
  },

  components: {
  }
}
</script>

<style>
.room-img {
  width: 100%;
  margin-top: 40px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}

</style>
