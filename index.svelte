<script>
   
   import DraggableModal from '../../lib/DraggableModal/index.svelte';

    let showModal = false;

    const toggleModal = () => {
        showModal = !showModal;
    }
</script>

<div>Another content</div>
<button style="width: 150px" on:click={toggleModal} >Show Modal</button>
{#if showModal}
<DraggableModal left={200} top={200} title="Drag Me">
    Draggable Modal Content
</DraggableModal>
{/if}