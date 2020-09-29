<script context="module">	

import {posts} from './store.js'
export function preload() {
  return { posts };  
}
</script>

<script>
	export let posts;
</script>

<svelte:head>
	<title>Blog</title>
</svelte:head>

<h1>Recent posts</h1>

<ul>
	 {#each posts as post}
	 	<li><a href="blog/{post.slug}">{post.title}</a></li>
	 {/each}
</ul>
