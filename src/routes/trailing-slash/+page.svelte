<script lang="ts">
    import {page} from "$app/stores";
    const url = $page.url.pathname
    const hasTrailingSlash = url.slice(-1) == "/"
</script>

<h1>Trailing Slash</h1>
<h2>{$page.url} -- {hasTrailingSlash? 'has a trailing slash, the below link will work' : 'no trailing slash, the below link will fail'}</h2>
<a href="./result">Check result</a>

<button on:click={()=>{window.location.reload()}}>Refreshing will result in a correctly formatted trailing slash</button>