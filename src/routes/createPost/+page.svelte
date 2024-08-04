<script>
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
  
      // Aquí puedes realizar la lógica para guardar el nuevo post en tu aplicación
      console.log('Nuevo post:', newPost);
  
      // Limpia los campos del formulario después de enviar los datos
      title = '';
      author = '';
      date = '';
      content = '';
    }
  </script>
  
  <style>
    .form {
      display: flex;
      flex-direction: column;
      margin: 20px;
    }
  
    .form-field {
      display: flex;
      flex-direction: column;
      margin-bottom: 10px;
    }
  
    .form-field label {
      font-weight: bold;
      margin-bottom: 5px;
    }
  
    .form-field input,
    .form-field textarea {
      padding: 5px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
  
    .submit-button {
      padding: 8px 12px;
      background-color: #007bff;
      color: #fff;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
  </style>
  
  <div class="form">
    <div class="form-field">
      <label for="title">Título</label>
      <input id="title" bind:value={title} type="text" />
    </div>
    <div class="form-field">
      <label for="author">Autor</label>
      <input id="author" bind:value={author} type="text" />
    </div>
    <div class="form-field">
      <label for="date">Fecha</label>
      <input id="date" bind:value={date} type="text" />
    </div>
    <div class="form-field">
      <label for="content">Contenido</label>
      <textarea id="content" bind:value={content}></textarea>
    </div>
    <button class="submit-button" on:click={handleSubmit}>Agregar post</button>
  </div>