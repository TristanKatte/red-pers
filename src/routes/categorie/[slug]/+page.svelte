<script>
    /** @type {import('./$types').PageData} */
    export let data;

    const dateFormat = {
        month: 'short',
        day: 'numeric',
    };
    
    import Footer from '$lib/Organism/Footer.svelte';
    import Header from '$lib/Organism/Header.svelte';
</script>

<Header/>

<main>
    {#if data.posts}
    {#each data.posts as post}
    <!-- @html means: there is html in this string, render it -->
        <div class="posts-grid">
            <div class="post-container">
            <a href="/{post.slug}">
            <h3>{@html post.title.rendered}</h3>
        </a>
        <p>{@html post.excerpt.rendered}</p>
        <img src={post.yoast_head_json.og_image[0].url} alt="Artikel afbeelding" width="350" height="350">
        <p>{(new Date(post.date)).toLocaleDateString("nl-NL", dateFormat)}</p>
        <p>{post.yoast_head_json.twitter_misc["Geschatte leestijd"]}</p>
        <p>{post.yoast_head_json.author}</p>
        </div>
    </div>
    {/each}
{:else}
    <!-- This will show if no posts are available -->
    <p>No posts available</p>
{/if}
</main>

<Footer />

<style>
  main {
    border: 1px solid black;
    padding: 1.5em;
  }

  .posts-grid {
    display: flex;
    flex-wrap: wrap;
    border-bottom: 1px solid #787878; 

  }
  
.post-container {
    padding-bottom: 1em; 
    margin-bottom: 1em; 
    
}
  
  .post-container:last-child {
    border-bottom: none;
    margin-bottom: 0;
    padding-bottom: 0;
  }


</style>