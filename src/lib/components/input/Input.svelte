<script lang="ts">
    export let value: string;
    export let type: string;
    export let label: string;

    function handleChange(e: any) {
        value= e.target.value;
    }
</script>

<style>
    .inputField {
      display: flex;
      flex-direction: column;
      margin: 15px 0
    }

    input, textarea {
        background-color: transparent;
        border-radius: 10px;
        border: 1px solid #468189;
        padding: 15px;
        color: #F4E9CD;
    }

    textarea:focus,
    input:focus {
        outline: none;
    }

    textarea {
        height: 80px;
    }
</style>

<div class="inputField">    
    {#if (type === "textarea")}
        <textarea placeholder={label} value={value} on:input={handleChange} />
    {:else}
        <input placeholder={label} type="text" value={value} on:input={handleChange} />
    {/if}
</div>