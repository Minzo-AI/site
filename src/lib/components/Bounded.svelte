<!-- src/lib/components/Bounded.svelte -->
<script lang="ts">
    export let tag: keyof HTMLElementTagNameMap = 'section';
    export let className: string = '';
  </script>
  
  <svelte:element
    this={tag}
    {...$$restProps}
    class={`px-4 py-14 first:pt-10 md:px-6 md:py-20 lg:py-24 ${className}`}
  >
    <div class="mx-auto flex w-full max-w-6xl flex-col items-center">
      <slot />
    </div>
  </svelte:element>