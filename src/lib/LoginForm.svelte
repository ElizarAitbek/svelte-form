<script>
   import { Button } from '$lib/components/ui/button/index.js';
   import { Input } from '$lib/components/ui/input';
   import { Label } from '$lib/components/ui/label';
   import { Checkbox } from '$lib/components/ui/checkbox/index.js';

   let checked = false;
</script>

<main
   class="flex flex-col m-auto rounded-[27px] text-white py-10 px-10 items-center w-96 bg-[#171929] mb-10"
>
   <p class="text-center font-lg">For business enquiries please use the form below</p>
   <span class="text-sm font-thin text-[#797ea3]">*Required</span>

   <form class="flex gap-3 mt-2.5 flex-col">
      <Label for="name">Name*</Label>
      <Input id="name" type="text" />

      <Label for="company">Company*</Label>
      <Input id="company" type="text" />

      <Label for="email">E-mail*</Label>
      <Input id="email" type="email" />

      <Label for="phone">Phone*</Label>
      <Input id="phone" type="text" />

      <Label for="subject">Subject*</Label>
      <Input id="subject" type="text" />

      <Label for="message">Message*</Label>
      <Input id="message" type="text" />

      <section class="flex justify-center items-center gap-3">
         <Checkbox id="terms" bind:checked aria-labelledby="terms-label" />
         <Label id="terms-label" for="terms" class="font-thin text-[#797ea3]">
            I accept
            <a
               class="border-b border-[#797ea3] text-[#797ea3]"
               href="https://en.wikipedia.org/wiki/Privacy_policy"
               target="_blank"
            >
               Terms and Privacy Policy
            </a>
         </Label>
      </section>

      <Button
         class="bg-[#797ea3] w-32 h-11 text-lg rounded-full m-auto"
         size="sm"
         variant="default"
      >
         Send
      </Button>
   </form>
</main>
