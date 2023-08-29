<!-- svelte-ignore a11y-click-events-have-key-events -->
<script>
    export let f, s;
    const close = e => {
        if (!!e) e.preventDefault();
        f.upgradeLvl2('modals', 'exampleBase', 'example', false);
    }
    // add event to close with scape
    window.addEventListener('keydown', e => {
        if (e.key === 'Escape') close(e);
    });
</script>

<div
    class={`modal_info`}
    on:click={e => close(e)}
    >
    <div 
        class={`flex justify-center flex-row flex-wrap modal_container modal_container_50 pb-5 pt-5 my_modal`}
        on:click={e => e.stopPropagation()}
        >
        <div class="flex flex-row flex-wrap justify-around w-full">
            Tema Cambiado a {s?.theme || 'White'}
        </div>
    </div>
</div>

<style lang="scss">
    .modal_info {
        background-color: #0008;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100vh;
        z-index: 2000;
        overflow-y: scroll;
        display: flex;
        justify-content: center;
        align-items: start;
        z-index: 1000;

        .my_modal {
            border: 1px var(--my-minor) solid;
        }
        .modal_container {
            margin-top: 10vh;
            height: 15vh;
            max-height: 85vh;
            border-radius: 15px;
            animation: fadeIn .4s;
            width: 80%;
            overflow: hidden;
            overflow-y: scroll;
            position: relative;
            background-color: var(--my-major);
            
        }
        /* 50, 60, 70, 80, 90 */
        .modal_container_50 {
            width: 50%;
        }
        .modal_container_60 {
            width: 60%;
        }
        .modal_container_70 {
            width: 70%;
        }
        .modal_container_80 {
            width: 80%;
        }
        .modal_container_90 {
            width: 90%;
        }
    }
</style>