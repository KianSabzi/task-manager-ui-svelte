<script>
    import {Input, Select, Label, Button} from 'flowbite-svelte';


    let selected;
    let categories = [
        { value: '01', name: 'زبان انگلیسی' },
        { value: '02', name: 'کنکور ارشد' },
        { value: '03', name: 'دانشگاه' }
    ];
</script>


<div class="container space-y-4 my-8">
    <Input class="w-full text-black-500" placeholder="عنوان تسک"/>
    <div class="grid grid-cols-2">
        <Label class="">
                یک دسته بندی را انتخاب کنید
                <Select class="mt-2" items={categories} bind:value={selected} />
        </Label>
        <Button class="primary mr-4" type="submit">ثبت</Button>
    </div>
</div>

