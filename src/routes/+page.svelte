<script lang="ts">
    import Post from '$lib/components/post/Post.svelte';
    import { postExamples } from '$lib/test/testData'
  </script>
  
  <style>
    .feed {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-gap: 20px;
      margin: 0 1rem;
    }
  </style>
  
  <div class="feed">
    {#each postExamples as item}
      <Post 
        nickname={item.nickname} 
        username={item.username}
        date={item.postContent.date}
        title={item.postContent.title}
        text={item.postContent.text} 
        />
    {/each}
  </div>