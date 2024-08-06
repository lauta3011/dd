<script>
  import Input from "$lib/components/input/Input.svelte";
  
  let search = "";
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
    
    nav {
        display: inline-flex;
    }

    a {
      transition: .5s;
      padding: 8px 12px;
      margin-right: 15px;
      text-decoration: none;
      color: #fff;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

    a:hover {
      background-color: #77ACA2;
    }
  </style>
  
<div class="header">
    <input
        class="search-input"
        type="text"
        placeholder="Buscar..."
        on:input={event => onSearch(event.target.value)}
    />
    <!-- <Input label="Busca algo" type="text" bind:value={search} /> -->

    <nav>
        <a href="/">home</a>
        <a href="/createPost">
            + post
        </a>

        <!-- agregar screen de perfil -->
        <a>
          perfil
        </a>    
    </nav>
</div>