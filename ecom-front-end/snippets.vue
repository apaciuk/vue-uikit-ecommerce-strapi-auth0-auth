<div class="uk-margin-small">
						<div class="uk-inline uk-width-1-1">
							<span class="uk-form-icon uk-form-icon-flip" data-uk-icon="icon: lock"></span>
							<input class="uk-input uk-border-pill" required placeholder="Password" type="password">
						</div>
					</div>
					<div class="uk-margin-small">
						<label><input class="uk-checkbox" type="checkbox"> Keep me logged in</label>
					</div>






					 <ul v-if="$store.state.authenticated">
       <li><NuxtLink to="/">Home</NuxtLink></li>
       <li><NuxtLink to="/profile">Profile</NuxtLink></li>
       <li><a class="logout" @click="userLogout">Logout</a></li>
     </ul>
     <ul v-else>
       <li>
         <a class="logout">Magic Nuxt Demo</a>
       </li>
     </ul>


     	<div class="drop-nav uk-dropdown" data-uk-dropdown="mode: click; offset: 20;animation: uk-animation-slide-bottom-small; duration: 150">
									<h4 class="uk-margin-small-bottom uk-margin-remove-adjacent">Account</h4>
								    <hr>
                                <ul class="uk-list uk-list-space">
                                 <li><span class="uk-margin-small-right" data-uk-icon="icon: user"></span><NuxtLink v-if="$auth.loggedIn" to="/profile">User Profile</NuxtLink></li>
									  <li><span class="uk-margin-small-right" data-uk-icon="icon: cog"></span>Account</li>
									   <li><span class="uk-margin-small-right" data-uk-icon="icon: mail"></span>Messages</li>
									    <a class="logout" data-uk-icon="icon: sign-out" v-if="$auth.loggedIn" @click="$auth.logout()">Logout</a>
										<a class="login" data-uk-icon="icon: sign-in" v-else @click="$auth.loginWith('auth0')">Login</a>

                                        
									
									</ul>
                               
									<hr>
									
								</div>
							</li>


							  <div class="label">Email</div>
   <div class="profile-info">{{ $store.state.user.email }}</div>

   <div class="label">Issuer</div>
   <div class="profile-info">{{ $store.state.user.issuer }}</div>

   <div class="label">Public Address</div>
   <div class="profile-info">{{ $store.state.user.publicAddress }}</div>

   // Middleware functions

   export default function ({ store, redirect }) {
    // If the user is not authenticated, redirect to login page.
    if (!store.state.authenticated) {
      return redirect('/login');
    }
}

// S6tore mutations

import { auth0 } from '../plugins/auth0'

export const state = () => ({
    user: null,
    authenticated: false
})

export const mutations = {
SET_USER_DATA(state, userData) {
    state.user = userData;
    state.authenticated = true;
},
CLEAR_USER_DATA(state) {
    state.user = null;
    state.authenticated = false;
    this.$router.push('/login');
}
}
export const actions = {
    async login({ commit }, email) {
      await magic.auth.loginWithMagicLink(email);
      const metadata = await magic.user.getMetadata();
      commit('SET_USER_DATA', metadata);
    },
    async logout({ commit }) {
      await magic.user.logout();
      commit('CLEAR_USER_DATA');
    },
};