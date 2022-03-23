<script>
    export let text;
    export let color;
</script>


<div class="container" style="background-color: var({color}); !important">
    <p>{text}</p>
</div>


<style>
    .container {
        display: flex;
        flex-wrap: nowrap;
        align-items: center;
        justify-content: center;
        background-color: var(--green);
        border-radius: 10px;
        width: 150px;
        height: 25px;
        padding: 2px;
    }

    p {
        font-size: 15px;
        color: white;
        font-weight: 100;
        text-transform: uppercase;
    }
</style>