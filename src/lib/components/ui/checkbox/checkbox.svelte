<script>
   import { Checkbox as CheckboxPrimitive } from 'bits-ui';
   import Check from 'lucide-svelte/icons/check';
   import Minus from 'lucide-svelte/icons/minus';
   import { cn } from '$lib/utils.js';
   let className = undefined;
   export let checked = false;
   export { className as class };
</script>

<CheckboxPrimitive.Root
   class={cn(
      'border-[#3f4363] ring-offset-background focus-visible:ring-ring data-[state=checked]:bg-[#2c2f47] data-[state=checked]:text-primary-foreground peer box-content h-8 w-8 shrink-0 rounded-lg border-2 focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-offset-2 disabled:cursor-not-allowed disabled:opacity-50 data-[disabled=true]:cursor-not-allowed data-[disabled=true]:opacity-50',
      className,
   )}
   bind:checked
   {...$$restProps}
   on:click
>
   <CheckboxPrimitive.Indicator
      class={cn('flex h-8 w-8 items-center justify-center text-current')}
      let:isChecked
      let:isIndeterminate
   >
      {#if isChecked}
         <Check class="h-7 w-7" />
      {:else if isIndeterminate}
         <Minus class="h-7 w-7" />
      {/if}
   </CheckboxPrimitive.Indicator>
</CheckboxPrimitive.Root>
