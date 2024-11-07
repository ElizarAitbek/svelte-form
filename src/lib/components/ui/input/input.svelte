<script>
   import { cn } from '$lib/utils.js';
   let className = undefined;
   export let value = undefined;
   export { className as class };
   export let readonly = undefined;
</script>

<input
   class={cn(
      'border-b border-[#3f4363] bg-[#171929] flex h-10 w-full rounded-none px-3 py-2 text-xl focus:border-b-2 focus:border-white focus-visible:outline-none focus-visible:ring-0 disabled:cursor-not-allowed disabled:opacity-50',
      className,
   )}
   bind:value
   {readonly}
   on:blur
   on:change
   on:click
   on:focus
   on:focusin
   on:focusout
   on:keydown
   on:keypress
   on:keyup
   on:mouseover
   on:mouseenter
   on:mouseleave
   on:mousemove
   on:paste
   on:input
   on:wheel|passive
   {...$$restProps}
/>
