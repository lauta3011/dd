<script lang="ts">
    import Card from '$lib/components/post/Post.svelte';
    import { postExamples } from '$lib/test/testData'

    interface CardData {
      title: string;
      content: string;
    }
    // let data: CardData[] = [
    //   { title: 'Título 1', content: 'Contenido 1' },
    //   { title: 'Título 2', content: 'Contenido 2' },
    //   { title: 'Título 3', content: 'Contenido 3' },
    //   { title: 'Título 4', content: 'Contenido 4' },
    //   { title: 'Título 5', content: 'Contenido 5' },
    //   { title: 'Título 6', content: 'Contenido 6' },
    //   { title: 'Título 7', content: 'Contenido 7' },
    //   { title: 'Título 8', content: 'Contenido 8' }
    // ];
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
      <Card 
        nickname={item.nickname} 
        username={item.username}
        date={item.postContent.date}
        text={item.postContent.text} 
        />
    {/each}
  </div>