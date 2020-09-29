<script context="module">
import {getPost} from './store'

export async function preload({ params }) {
  return {post : getPost(params.slug)}
}
</script>

<script>
	export let post;
</script>

<svelte:head>
	<title>{post.title}</title>
</svelte:head>

<h1>{post.title}</h1>

<div class="content">
	{@html post.html}
</div>
