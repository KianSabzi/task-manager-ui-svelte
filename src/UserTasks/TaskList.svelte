<script>
// @ts-nocheck
    import { Listgroup, ListgroupItem, NavHamburger } from 'flowbite-svelte';
    import { LinkOutline, StarOutline} from "flowbite-svelte-icons"
    import TaskDetails from './TaskDetails.svelte';
    import TaskBox from './TaskBox.svelte';
    export let tasks;
</script>

<style>

</style>

<section id="tasklist">
    <h3 class="py-4 text-center text-xl font-medium text-gray-900 dark:text-white">کنکور ارشد</h3>
    {#each tasks as task}
    <TaskBox 
    title = {task.title}
    dueDate = {task.dueDate}
    progress = {task.progress}
    />
    {/each}

</section>