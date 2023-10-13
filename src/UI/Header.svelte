<script>
      import { Button, Input, Navbar, NavBrand, NavLi, NavUl, NavHamburger, Avatar, Dropdown, DropdownItem, DropdownHeader, DropdownDivider  } from 'flowbite-svelte';
      import { SearchOutline } from 'flowbite-svelte-icons';

</script>


<Navbar let:NavContainer color="blue"  fluid={true}>
    <NavContainer class="border px-5 py-2 rounded-lg bg-white dark:bg-gray-600">
      <NavBrand href="/">
        <img src="src/assets/svelte.svg" class="mr-3 h-6 sm:h-9" alt="Flowbite Logo" />
      </NavBrand>
      <div class="flex md:order-2">
        <Button color="none" data-collapse-toggle="mobile-menu-3" aria-controls="mobile-menu-3" aria-expanded="false" class="md:hidden text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 focus:outline-none focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-700 rounded-lg text-sm p-2.5 mr-1">
          <SearchOutline class="w-5 h-5" />
        </Button>
        <div class="hidden relative md:block ml-10 w-96">
          <div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
            <SearchOutline class="w-4 h-4" />
          </div>
          <Input id="search-navbar" class="pl-10" placeholder="جستجو..." />
        </div>
        <Button pill color="light" id="avatar-menu" class="!p-1">
            <Avatar src="src/assets/images/user-profile1.png" class="mr-2" />
            مرتضی سبزی
          </Button>
        <NavHamburger />
        <Dropdown placement="bottom" class="text-center" triggeredBy="#avatar-menu">
            <DropdownHeader>
              <span class="block text-md">mksabzi</span>

              <span class="block truncate text-sm font-medium mt-2">sabzi@test.com</span>
            </DropdownHeader>
            <DropdownItem class="text-center" >پنل کاربری</DropdownItem>
            <DropdownItem class="text-center">پیام ها</DropdownItem>
            <DropdownItem class="text-center">پرداخت ها</DropdownItem>
            <DropdownDivider />
            <DropdownItem class="text-center">خروج</DropdownItem>
          </Dropdown>
      </div>
      <NavUl>
        <!-- <NavLi href="/">Home</NavLi>
        <NavLi href="/about">About</NavLi>
        <NavLi href="/docs/components/navbar">Navbar</NavLi>
        <NavLi href="/pricing">Pricing</NavLi>
        <NavLi href="/contact">Contact</NavLi> -->
      </NavUl>
    </NavContainer>
  </Navbar>

