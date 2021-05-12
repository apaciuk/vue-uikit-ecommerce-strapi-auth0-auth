<template>
<header id="site-head">
			<div class="uk-container uk-container-expand">
				<div class="uk-grid uk-grid-medium uk-flex uk-flex-middle uk-flex-between" data-uk-grid>
					<div class="uk-width-auto" id="logo">
						<a href="#" class="uk-logo" title="eCommerce"><img src="logo.png" alt="Logo"></a>
					</div>
				    <div class="uk-width-auto">
					    <ul class="uk-subnav" data-uk-margin>
						  <li class="uk-visible@s"><NuxtLink to="/">Home</NuxtLink></li>
						  	  <li class="uk-visible@s"><NuxtLink to="/">About</NuxtLink></li>
							<li class="uk-visible@s"><NuxtLink to="/contact">Collections</NuxtLink></li>
								  <li class="uk-visible@s"><NuxtLink to="/">Categories</NuxtLink></li>
							<li class="uk-visible@s"><NuxtLink to="/contact">Best Sellers</NuxtLink></li>
									  <li class="uk-visible@s"><NuxtLink to="/">Instagram</NuxtLink></li>
							<li class="uk-visible@s"><NuxtLink to="/contact">Trending</NuxtLink></li>
								  <li class="uk-visible@s"><NuxtLink to="/">Sale</NuxtLink></li>
							<li class="uk-visible@s"><NuxtLink to="/contact">New</NuxtLink></li>
								<li class="uk-visible@s"><NuxtLink to="/contact">Journal</NuxtLink></li>
							<li class="uk-visible@s"><NuxtLink to="/contact">Contact</NuxtLink></li>
				
							
		       
								<li class="uk-visible@s">
								<a href="#" data-uk-icon="icon:cart"></a>
								<div class="drop-nav uk-dropdown" data-uk-dropdown="mode: click; offset: 20;animation: uk-animation-slide-bottom-small; duration: 150">
									<h4 class="uk-margin-small-bottom uk-margin-remove-adjacent">Shopping Cart</h4>
								    <hr>
<ul class="uk-nav-default uk-nav-parent-icon" data-uk-nav>
									
										
										<li><img src="purse.jpg" width="60" /><span class="uk-margin-small-left"></span>Mens Purse £240<span class="uk-margin-small-left" data-uk-icon="icon: trash"></span><span class="uk-margin-small-left" data-uk-icon="icon: pencil"></span></li>
									</ul>
                                    <hr>
									<a href="#" class="uk-button uk-button-secondary uk-width-1-1">CHECKOUT</a>
									<hr>
									
								</div>
							</li>
							<li class="uk-visible@s">
								<a href="#" data-uk-icon="icon:heart"></a>
								<div class="drop-nav uk-dropdown" data-uk-dropdown="mode: click; offset: 20;animation: uk-animation-slide-bottom-small; duration: 150">
									<h4 class="uk-margin-small-bottom uk-margin-remove-adjacent">Wishlist</h4>
									<hr>
<ul class="uk-nav-default uk-nav-parent-icon" data-uk-nav>
								
									<li><img src="purse.jpg" width="60" /><span class="uk-margin-small-left"></span>Mens Purse £240<span class="uk-margin-small-left" data-uk-icon="icon: trash"></span><span class="uk-margin-small-left" data-uk-icon="icon: pencil"></span></li>
									</ul>
                                    <hr>
									<a href="#" class="uk-button uk-button-secondary uk-width-1-1">ADD ALL TO CART</a>
									<hr>
									
								</div>
							</li>
						
									<li class="uk-visible@s">
								<a href="#" data-uk-icon="icon:user"></a>
								<div class="drop-nav uk-dropdown" data-uk-dropdown="mode: click; offset: 20;animation: uk-animation-slide-bottom-small; duration: 150">
									<h4 class="uk-margin-small-bottom uk-margin-remove-adjacent">Account</h4>
								    <hr>
<ul class="uk-list uk-list-space">
									 <li><span class="uk-margin-small-right" data-uk-icon="icon: user"></span>User Profile</li>
									  <li><span class="uk-margin-small-right" data-uk-icon="icon: cog"></span>Account</li>
									   <li><span class="uk-margin-small-right" data-uk-icon="icon: mail"></span>Messsages</li>
									    <li><span class="uk-margin-small-right" data-uk-icon="icon: sign-out"></span>Logout</li>
									</ul>
                               
									<hr>
									
								</div>
							</li>
						<li class="uk-hidden@s"><a data-uk-navbar-toggle-icon data-uk-toggle href="#offcanvas-nav"></a></li>
						</ul>
					</div>
				</div>
			</div>
		</header>
     <!--/HEADER-->
</template>
<script>
export default {
}
</script>
<style scoped>
#site-head {
padding-right: 50px;
padding-left: 30px;
}
#logo {
padding-bottom: 6px;
}
h4.uk-margin-small-bottom {
text-transform: uppercase;
font-size: 1em;
}
li.uk-visible@s a {
padding-right: 20px;
}
</style>
