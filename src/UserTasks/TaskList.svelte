<script>
// @ts-nocheck
    import { Listgroup, ListgroupItem } from 'flowbite-svelte';
    import { StarOutline} from "flowbite-svelte-icons"
    export let tasks;
</script>

<style>

</style>

<section id="tasklist">
    <h3 class="py-4 text-center text-xl font-medium text-gray-900 dark:text-white">کنکور ارشد</h3>
    <Listgroup active items={tasks} let:item class="w-full md:w-auto space-y-3 p-2.5 relative">
        <div class="flex flex-col p-2">
            <div class=""><h2>{item.title}</h2></div>
            <div><span class="text-orange-500 float-right">{item.dueDate}</span></div> 
        </div>
        <i class="absolute left-4 text-blue-700"><StarOutline class=""></StarOutline></i>        
    </Listgroup>

</section>