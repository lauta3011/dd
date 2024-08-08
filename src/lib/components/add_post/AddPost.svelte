<script>
    import FormButtons from "$lib/components/form_buttons/FormButtons.svelte";
    import Input from "$lib/components/input/Input.svelte";

    export let handleClick = () => {};

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

        handleClick();
    }
  </script>
  
  <style>
    .background-modal {
        position: absolute;
        z-index: 1;
        background-color: #04192566;
        width: 100%;
        height: 100%;
    }
    .form {
        position: absolute;
        display: flex;
        flex-direction: column;
        background-color: #041925;
        z-index: 1;
        border: 1px solid #468189;
        border-radius: 15px;
        color: #F4E9CD;
        margin: 20px;
        padding: 20px;
    }
  </style>
  
  <div class="background-modal"></div>
  <div class="form">
    <h1>Crea un nuevo post</h1>
    <Input label="* Titulo" type="text" bind:value={title} />
    <Input label="* Contenido" type="textarea" bind:value={content} />

    <FormButtons handleCancel={() => handleCancel()} handleSubmit={() => handleSubmit()} />
  </div>