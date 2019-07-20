<template>
  <div id="app">
     
    <TweetComponent v-for="tweet in tweets" :key="tweet.id" :tweet="tweet"></TweetComponent>
    
  </div>
</template>

<script>
import TweetComponent from "./components/tweet-component"
export default {
  name: "app",
  data() {
    return {
      tweets: [
        {
          id: 1,
          name: "James",
          handle: "@jokerjames",
          img: "/images/james.png",
          tweet: "If you don't succeed, dust yourself off and try again.",
          likes: 10
        },
        {
          id: 2,
          name: "Fatima",
          handle: "@fantasticfatima",
          img: "/images/fatima.png",
          tweet: "Better late than never but never late is better.",
          likes: 12
        },
        {
          id: 3,
          name: "Xin",
          handle: "@xeroxin",
          img: "/images/xin.png",
          tweet: "Beauty in the struggle, ugliness in the success.",
          likes: 18
        }
      ]
    };
  },
  components:{
    TweetComponent
  }
}
  
</script>

<style>
html, body {
  height: 100%;
  padding-top: 10px;
  background: #e6ecf1;
}

#app {
  height: 100%;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
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
