<script>
    import FormButtons from "$lib/components/form_buttons/FormButtons.svelte";
    import Input from "$lib/components/input/Input.svelte";
    import { goto } from '$app/navigation';

    let title = '';
    let author = '';
    let date = '';
    let content = '';
  
    function handleSubmit() {
      const newPost = {
        title,
        author,
        date,
        content,
      };
  
      console.log('Nuevo post:', newPost);
    }

    function handleCancel() {
        title = '';
        author = '';
        date = '';
        content = '';

        goto('/');
    }
  </script>
  
  <style>
    .form {
      display: flex;
      border: 1px solid #468189;
      border-radius: 15px;
      color: #F4E9CD;
      flex-direction: column;
      margin: 20px;
      padding: 20px;
    }
  </style>
  
  <div class="form">
    <h1>Crea un nuevo post</h1>
    <Input label="* Titulo" type="text" bind:value={title} />
    <Input label="* Contenido" type="textarea" bind:value={content} />

    <FormButtons handleCancel={() => handleCancel()} handleSubmit={() => handleSubmit()} />
  </div>