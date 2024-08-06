<script>
    export let handleCancel;
    export let handleSubmit;
</script>

<style>
    .container {
        display: flex;
        justify-content: end;
    }

    button {
        padding: 5px 25px;
        margin: 0 15px;
        border: none;
        border-radius: 4px;
        cursor: pointer;
    }

    button:hover {
        transition: .1s;
        transform: translateY(-2px);
    }

    .cancel {
        background-color: transparent;
        color: #fff
    }

    .confirm {
        background-color: #468189;
        color: #fff
    }

</style>

<div class="container">
    <button on:click={handleCancel} class="cancel">cancelar</button>
    <button on:click={handleSubmit} class="confirm">agregar</button>
</div>