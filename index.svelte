<script>
   
   import DraggableModal from '../../../lib/Draggable/index.svelte';

    let showModal = false;

    const toggleModal = () => {
        showModal = !showModal;
    }
</script>

<div>Sub-module content</div>
<br />
<p>This sub-module can use the common components from the app shell</p>
<button style="width: 150px" on:click={toggleModal} >{showModal ? 'Hide Modal' : 'Show Modal'}</button>
{#if showModal}
<DraggableModal left={200} top={200} title="Drag Me">
    Draggable Modal Content
</DraggableModal>
{/if}