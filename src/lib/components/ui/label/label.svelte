<script>
   import { Label as LabelPrimitive } from 'bits-ui';
   import { cn } from '$lib/utils.js';
   let className = undefined;
   export { className as class };
</script>

<LabelPrimitive.Root
   class={cn('text-sm peer-focus:text-white transition-colors font-medium leading-none', className)}
   {...$$restProps}
   on:mousedown
>
   <slot />
</LabelPrimitive.Root>
