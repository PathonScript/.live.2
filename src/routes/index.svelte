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
      <h1 class="text-4xl sm:text-8xl engtle">👋</h1>
      <Typewriter
        mode="loop"
      >
      <h1 class="hello">Hello</h1>
      <h1 class="hello">Goodendag</h1>
      <h1 class="hello">こんにちは</h1>
      <h1 class="hello">Hola</h1>
      <h1 class="hello">Bonjour</h1>
      <h1 class="hello">안녕하세요
  </h1>


      </Typewriter>
    </div>

    <h1 class="flex text-6xl text-white mx-5">I'm Pat</h1>

    <div class="grid grid-cols-3 sm:grid-cols-5 h-24 w-full">

      <a href="/#about" class="grid card">
        <div>
          <h1 class="text-red-500">About Me</h1>
        </div>
      </a>

      <a href="https://twitter.com/patatotota" class="grid card" target="_blank">
        <div>
          <h1>Twitter</h1>
        </div>
      </a>
      
      <a href="https://github.com/pathonscript" class="grid card" target="_blank">
        <div>
          <h1>Github</h1>
        </div>
      </a>
      
      <a href="https://garden.patato.live" class="grid card" target="_blank">
        <div>
          <h1>Digital Garden</h1>
        </div>
      </a>
      
      <a href="https://discord.com" class="grid card" target="_blank">
        <div>
          <h1>Patato #0267</h1>
        </div>
      </a>
    </div>
  </div>
</div>

{#if $modal}
  <Modal closeModal={() => ($modal = false)} />
{/if}
