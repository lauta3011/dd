<script>  
  import AddPost from "$lib/components/add_post/AddPost.svelte";
  let addPost = false;
</script>
  
  <style>
    .header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 10px;
      margin-bottom: 25px;
      background-color: #041925;
      box-shadow: 0 0 15px 0 #041925;
    }
    
    .nav {
        display: inline-flex;
    }

    a, button {
      background-color: transparent;
      font-size: medium;
      transition: .5s;
      padding: 8px 12px;
      margin-right: 15px;
      text-decoration: none;
      color: #fff;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

    a:hover, button:hover {
      background-color: #77ACA2;
    }

    .post-modal {
      display: flex;
      justify-content: center;
    }
  </style>
  
{#if (addPost)}
  <div class="post-modal">
    <AddPost handleClick={() => addPost = false }/>
  </div>
{/if}

<div class="header">
    <div class="nav">
        <a>home</a>
        <button on:click={() => addPost = !addPost}>+ post</button>
    </div>    
</div>