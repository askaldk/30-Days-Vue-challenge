<template>
  <div id="app">
    <tweet v-for="tweet in tweets" :key="tweet.id" :name="tweet.name" :handle="tweet.handle" :likes="tweet.likes" :tweetss="tweet.tweetss" :img="tweet.img"></tweet>
  </div>
</template>

<script>
import tweet from "./components/tweet"

export default {
  name: "app",
  data() {
    return {
     tweets:[
  {
    id: 1,
    name: 'James',
    handle: '@jokerjames',
    img: '/images/james.png',
    tweetss: "If you don't succeed, dust yourself off and try again.",
    likes: 10,
  },
  { 
    id: 2,
    name: 'Fatima',
    handle: '@fantasticfatima',
    img: '/images/fatima.png',
    tweetss: 'Better late than never but never late is better.',
    likes: 12,
  },
  {
    id: 3,
    name: 'Xin',
    handle: '@xeroxin',
    img: '/images/xin.png',
    tweetss: 'Beauty in the struggle, ugliness in the success.',
    likes: 18,
  }
],        
    }
  },
  components: { tweet }
};
</script>

<style>
#app {
  align-items: center;
  justify-content: center;
  display: flex;
  flex-direction: column;
  height: 100vh;
}
#app .button {
  margin-bottom: 20px;
}

#app .tweet {
  width: 500px;
  margin: 0 auto;
  padding-bottom: 15px;
}

#app .box {
  margin-bottom: 0;
  border-radius: 0;
}

#app .content small {
  color: #00d1b2;
}

#app img {
  border-radius: 30px;
}

#app .level-item {
  padding-left: 10px;
  justify-content: flex-start;
  display: inline;
  color: #00d1b2;
}

#app input:focus {
  border-color: #00d1b2;  
}

#app .likes {
  padding: 0 7.5px;
}

#app input {
  font-weight: bold;
}

#app .tweets-move {
  transition: transform 1s;
}
</style>
