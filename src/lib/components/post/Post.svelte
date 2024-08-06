<script lang="ts">
  import PostButtons from "$lib/components/post_buttons/PostButtons.svelte";

  export let nickname: string;
  export let username: string;
  export let date: string;
  export let title: string;
  export let text: string;

  let onHover = false;
</script>

<style>
  .card {
    position: relative;
    background-color: #041925;
    height: 260px;
    overflow: hidden;
    border: 1px solid #468189;
    color: #F4E9CD;
    border-radius: 4px;
    margin-bottom: 10px;
    box-shadow: 0 0 15px 0 #041925;
  }

  .card-footer {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
  }

  .card-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
  }

  .content {
    padding: 10px;
  }

  .userInfo {
    display: flex;
    flex-direction: column;
  }

  .nickname {
    font-weight: bold;
  }

  .secondary {
    color: #888;
    font-size: 0.8em;
  }

  .onHover {
    transition: .1s;
    transform: translateY(-5px);
  }
</style>

<article class:onHover class="card" on:mouseenter={() => onHover = true } on:mouseleave={() => onHover = false } >
  <div class="content">

    <div class="card-header">
      <div class="userInfo">
        <span class="nickname">{nickname}</span>
        <span class="secondary">@{username}</span>
      </div>
      <div class="secondary">{date}</div>
    </div>
    
    <h3>{title}</h3>
    <p>{text}</p>
  </div>

  <div class="card-footer">
    <PostButtons />
  </div>
</article>