<script>
    export let onSearch = () => {};
    export let onAddPost = () => {};
</script>
  
  <style>
    .header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 10px;
      margin-bottom: 25px;
      background-color: #468189;
    }
  
    .search-input {
      margin-right: 10px;
      padding: 5px;
    }
  
    .add-post-button {
      padding: 8px 12px;
      background-color: #77ACA2;
      color: #fff;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
  </style>
  
<div class="header">
<input
    class="search-input"
    type="text"
    placeholder="Buscar..."
    on:input={event => onSearch(event.target.value)}
/>
<a class="add-post-button" href="/createPost">
    Agregar nuevo post
</a>
</div>