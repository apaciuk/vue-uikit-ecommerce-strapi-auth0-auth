<template>
       <div class="uk-width-medium uk-padding-small">
			<!-- login -->
			<form @submit.prevent="userLogin" class="toggle-class">
				<fieldset class="uk-fieldset">
					<div class="uk-margin-small">
						<div class="uk-inline uk-width-1-1">
							<span class="uk-form-icon uk-form-icon-flip" data-uk-icon="icon: user"></span>
							<input 
							v-model="name"
							class="uk-input uk-border-pill" 
							required 
							placeholder="Username" 
							type="text" />
						</div>
					</div>
					<div class="uk-margin-small">
						<div class="uk-inline uk-width-1-1">
							<span class="uk-form-icon uk-form-icon-flip" data-uk-icon="icon: user"></span>
							<input 
							v-model="email"
							class="uk-input uk-border-pill" 
							required 
							placeholder="Enter your email"
							type="email" />
						</div>
					</div>
					<div class="uk-margin-bottom">
						<button type="submit" class="uk-button uk-button-primary uk-border-pill uk-width-1-1">LOG IN</button>
					</div>
				</fieldset>
			</form>
			<!-- /login -->

			<!-- recover password -->
			<form class="toggle-class" action="login-dark.html" hidden>
				<div class="uk-margin-small">
					<div class="uk-inline uk-width-1-1">
						<span class="uk-form-icon uk-form-icon-flip" data-uk-icon="icon: mail"></span>
						<input class="uk-input uk-border-pill" placeholder="E-mail" required type="text">
					</div>
				</div>
				<div class="uk-margin-bottom">
					<button type="submit" class="uk-button uk-button-primary uk-border-rounded uk-width-1-1">Send Magic Link</button>
				</div>
			</form>
			<!-- /recover password -->
			
			<!-- action buttons -->
			<div>
				<div class="uk-text-center">
					<a class="uk-link-reset uk-text-small toggle-class" data-uk-toggle="target: .toggle-class ;animation: uk-animation-fade">Forgot your password?</a>
					<a class="uk-link-reset uk-text-small toggle-class" data-uk-toggle="target: .toggle-class ;animation: uk-animation-fade" hidden><span data-uk-icon="arrow-left"></span> Back to Login</a>
				</div>
			</div>
			<!-- action buttons -->
		</div>

</template>

<script>
export default {
 data() {
   return {
     email: '',
	 name: ''
   }
 },
 mounted() {
   // If the user is authenticated, redirect to profile page.
   if (this.$store.state.authenticated) {
     this.$router.push('/profile')
   }
 },
 methods: {
   async userLogin() {
     this.$store
       .dispatch('login', {
         email: this.email,
		 name: this.name
       })
       .then(() => {
         this.$router.push('/profile')
       })
       .catch((err) => {
         console.log(err)
       })
   },
 },
}
</script>