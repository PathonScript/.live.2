<script lang="ts">
  import Typewriter from 'svelte-typewriter'

  import Modal from '$lib/components/Modal.svelte';
  import { modal } from '$lib/store';
  import { goto } from '$app/navigation';

  let clicked = 0;
</script>

<div class="fullflex">
  <div class="flex flex-col w-3/4">
    <div class="flex flex-row">
      <h1 class="text-8xl engtle">👋</h1>
      <Typewriter
        mode="loop"
      >
      <h1 class="flex text-8xl text-white engtle">Hello</h1>
      <h1 class="flex text-8xl text-white engtle">Goodendag</h1>
      </Typewriter>
    </div>

    <h1 class="flex text-6xl text-white mx-5">I'm Pat</h1>

    <div class="grid grid-cols-5 h-24 w-full">

      <a href="/#about" class="grid card">
        <div>
          <h1>About Me</h1>
        </div>
      </a>
      
      <div class="grid card">
        <h1>Twitter</h1>
      </div>
      
      <div class="grid card">
        <h1>Github</h1>
      </div>
      
      <div class="grid card">
        <h1>Garden</h1>
      </div>
      
      <div class="grid card">
        <h1>Patato#0267</h1>
      </div>
    </div>
  </div>
</div>

{#if $modal}
  <Modal closeModal={() => ($modal = false)} />
{/if}
