{% include header.html %}
{% include navbar.html %}

<div class="container-fluid" style="height:100vw">
	<div class="row" style="height: 100%">
		<div class="col-sm-1 pt-6 bg-purple"></div>
		<div class="col-sm-4 pt-6 bg-purple">
			<h1 class="color-white pb-2" style="font-weight:300">Hi I'm Ellen and I'm a user experience designer</h1>
			<p class="h4 color-white-70" style="font-weight:300">I currently work at NASA JPL where I research and design for engineers and scientists</p>
		</div>
		<div class="col-sm-7">
			<ul class="pt-5 mt-5">
			  	{% for post in site.posts %}
				    <li>
				    	<a href="{{ post.url }}">{{ post.title }}</a>
				    </li>
			  	{% endfor %}
			</ul>
		</div>
	</div>
</div>


{% include footer.html %}