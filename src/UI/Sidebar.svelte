<script>
    import { Sidebar, SidebarGroup, SidebarItem, SidebarWrapper } from 'flowbite-svelte';
    import { ChartPieSolid, GridSolid, MailBoxSolid, UserSolid, ArrowRightToBracketSolid, FileEditSolid } from 'flowbite-svelte-icons';
    $: activeUrl = null
</script>


<Sidebar {activeUrl}>
    <SidebarWrapper>
      <SidebarGroup>
        <SidebarItem label="همه تسک ها" href="/">
          <svelte:fragment slot="icon">
            <ChartPieSolid class="w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white" />
          </svelte:fragment>
        </SidebarItem>
        <SidebarItem label="محبوب ترین ها" href="/docs/components/accordion">
          <svelte:fragment slot="icon">
            <GridSolid class="w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white" />
          </svelte:fragment>
        </SidebarItem>
        <SidebarItem label="برنامه ریزی شده" href="/docs/components/alert">
          <svelte:fragment slot="icon">
            <MailBoxSolid class="w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white" />
          </svelte:fragment>
        </SidebarItem>
        <SidebarItem label="امروز" href="/docs/components/sidebar">
          <svelte:fragment slot="icon">
            <UserSolid class="w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white" />
          </svelte:fragment>
        </SidebarItem>
        <!-- <SidebarItem label="Badge" href="/docs/components/badge">
          <svelte:fragment slot="icon">
            <ArrowRightToBracketSolid class="w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white" />
          </svelte:fragment>
        </SidebarItem> -->
      </SidebarGroup>
    </SidebarWrapper>
  </Sidebar>