<template>
<div class="uk-section uk-section-default uk-margin-top" uk-height-viewport="expand: true">
	<div class="uk-container uk-container-medium">
    <super-secret-div v-if="$auth.loggedIn"/>
    <div class="content">
      <h1>Hello, {{ $auth.loggedIn ? $auth.user.username : 'boogaloo' }}!</h1>
      <p>
        This is a super simple login page example of how to use <a href="https://nuxtjs.org" target="_blank">Vue JS</a>, <a href="https://nuxtjs.org" target="_blank">Nuxt.js</a> and <a href="https://auth0.com" target="_blank">Auth0</a> together.
      </p>
      <p v-if="$auth.loggedIn">
        Now that you're authenticated, maybe you should try going to our <NuxtLink to="/profile" class="link">Account Profile</NuxtLink>!
      </p>
      <p v-else>
        You're not authenticated yet. Maybe you want to <a @click="$auth.login()" class="link">sign in</a> and see what happens?
      </p>
    </div>
  </div>
  </div>
</template>

<script>
import SuperSecretDiv from '~/components/SuperSecretDiv'

export default {
  components: {
    SuperSecretDiv
  }
}
</script>

<style scoped>
.content {
  max-width: 750px;
  margin: 0 auto;
  text-align: center;
}
</style>
	
