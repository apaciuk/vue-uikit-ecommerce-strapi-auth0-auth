<template>
    <div class="uk-container">
    <img :src="user.picture"/>
    <p>Hi {{ user.email }}!</p>
    <p>This is a super secure profile page! Try loading this page again using the incognito/private mode of your browser.</p>
    <div class="label">Email</div>
   <div class="profile-info">{{ $store.state.user.email }}</div>

   <div class="label">Issuer</div>
   <div class="profile-info">{{ $store.state.user.issuer }}</div>

   <div class="label">Public Address</div>
   <div class="profile-info">{{ $store.state.user.publicAddress }}</div>
 </div>
</template>
<script>
export default {
  middleware: 'auth',
  computed: {
    user() {
      return this.$auth.user
    }
  }
}
</script>
<style scoped>
.content {
  text-align: center;
  padding-top: 20px;
}
img {
  width: 100px;
  height: 100px;
  border-radius: 100px;
  margin: 15px 0;
}
</style>
<script>
export default {}
</script>

 <style scoped>
.label {
 font-size: 12px;
 color: #6851ff;
 margin: 30px 0 5px;
}
.profile-info {
 font-size: 17px;
 word-wrap: break-word;
}
</style>