<template>
    <div class="tweet">
      <div class="box">
        <article class="media">
          <div class="media-left">
            <figure class="image is-64x64">
              <img :src="img">
            </figure>
          </div>
          <div class="media-content">
            <div class="content">
              <p>
                <strong>{{name}}</strong>
                <small>{{handle}}</small>
                <br>
                {{tweetss}}
              </p>
            </div>
            <div class="level-left">
              <a class="level-item">
                <span class="icon is-small">
                  <i class="fas fa-heart"></i>
                </span>
                <span class="likes">{{likes}}</span>
              </a>
            </div>
          </div>
        </article>
      </div>
      <div class="control has-icons-left">
        <input class="input is-small"
          placeholder="Tweet your reply..." />
        <span class="icon is-small is-left">
          <i class="fas fa-envelope"></i>
        </span>
      </div>
    </div>
</template>

<script>

export default {
  name:'tweet',
  props:{
    name:String,
    handle:String,
    tweetss:String,
    likes:Number,
    img:String

    
  }

}
</script>

