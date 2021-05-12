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