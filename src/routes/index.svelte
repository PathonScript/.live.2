<script lang="ts">
  import Modal from '$lib/components/Modal.svelte';
  import { modal } from '$lib/store';
  import { goto } from '$app/navigation';

  let clicked = 0;
</script>

<div class="fullflex">
  <div class="flex flex-col w-3/4">
    <h1 class="flex text-8xl text-white">👋 Goodendag</h1>
    <h1 class="flex text-6xl text-white mt-10">I'm Pat</h1>

    <div class="grid grid-cols-4 h-32 w-full">
      <div class="grid bg-slate-600 m-4"></div>
      <div class="grid bg-slate-600 m-4"></div>
      <div class="grid bg-slate-600 m-4"></div>
      <div class="grid bg-slate-600 m-4" />

    </div>
  </div>
</div>

{#if $modal}
  <Modal closeModal={() => ($modal = false)} />
{/if}
