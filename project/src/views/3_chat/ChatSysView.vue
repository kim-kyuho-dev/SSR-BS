<template>
    <html>
<head>
  <title>The Vue View</title>
  <link rel="stylesheet" type="text/css" href="./css/reset.css">
  <link rel="stylesheet" type="text/css" href="./css/style.css">
</head>
<body>
  <div id="app">
    <h1>THE VUE VIEW</h1>
    <div class="user">
      <div class="user-information">
        <div class="image-container">
          <img src="https://content.codecademy.com/courses/what-is-vue/profile.jpeg" alt="profile picture">
        </div>
        <h3>{{ username }}</h3>
      </div>
      <div class="user-bio" v-if="bio">
        <em>Bio: </em> {{ bio }}
      </div>
    </div>
    <div class="tweets">
      <div class="tweet" :key="(tweet, index)" v-for="tweet in tweets">
        <h3>{{ username }}</h3>
        <p>{{ tweet }}</p>
      </div>
    </div>
    <div class="settings">
      <h2>Settings</h2>
      <label for="username">Username</label>
      <input type="text" placeholder="Username" v-model="username" />
      <label for="bio">Bio</label>
      <textarea placeholder="Bio" v-model="bio"></textarea>
      <label for="tweet">New Tweet</label>
      <div class="new-tweet">
        <input type="text" placeholder="New Tweet" v-model="newTweet"/>
        <button v-on:click="tweets.push(newTweet)">Add Tweet</button>
      </div>
    </div>
  </div>
</body>
</html>
</template>
<script>
export default {
        username: 'CoderInTraining',
        newTweet: '',
        tweets: [
            'Started learning to code today. Wish me luck!',
            'Okay, I learned HTML, CSS, and JavaScript. But, how do I combine them together?? Send help.',
            'Today I start learning Vue. I got this.'
        ],
         bio: 'Excited future front-end  engineer.'
}
</script>
