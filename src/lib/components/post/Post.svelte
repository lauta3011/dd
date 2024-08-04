<script lang="ts">
  import ActionButtons from "$lib/components/actionButtons/ActionButtons.svelte";

  export let nickname: string;
  export let username: string;
  export let date: string;
  export let text: string;

  let onHover = false;
</script>

<style>
  .card {
    position: relative;
    height: 220px;
    overflow: hidden;
    border: 2px solid #468189;
    color: #F4E9CD;
    border-radius: 4px;
    margin-bottom: 10px;
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
    
    <p>{text}</p>
  </div>

  <div class="card-footer">
    <ActionButtons />
  </div>
</article>