<script>
    import { Button, Modal ,Label, Input,Datepicker,Checkbox , Textarea ,Fileupload,Helper, Dropzone} from 'flowbite-svelte';
    export let formModal = false;
    export let title;
    export let dueDate;
</script>

<style>

</style>


<Button on:click={() => (formModal = true)}>عنوان تسک</Button>

<Modal bind:open={formModal} size="md" autoclose={true} class="w-full">
  <form class="flex flex-col space-y-6" action="#">
    <h3 class="mb-4 text-xl font-medium text-gray-900 dark:text-white">جزییات تسک</h3>
    
    <Label class="space-y-2">
        <span class="float-right">عنوان تسک</span>        
    </Label>
    <Input class="" type="text" name="title" placeholder="عنوان جدید را وارد کنید" required />
    <div class="content-center">
        <div class="float-right">
            <Label class="flex flex-col space-y-2">
                <span class="">تاریخ سر رسید</span>
                <!-- <Datepicker name="dueDate" placeholder="تاریخ سررسید" class="space-y-2"></Datepicker> -->
            </Label>
        </div>       
        <div class="">
            <Label class="flex flex-col space-y-2">  
                <span class="">زمان یادآوری</span>              
                <!-- <Datepicker name="reminderDate" placeholder="تاریخ سررسید" class="space-y-2"></Datepicker> -->
             </Label>
        </div>
    </div>
    <Label class="space-y-2">
        <Dropzone class="h-20">
            <p class="mb-2 text-sm text-gray-500 dark:text-gray-400"><span class="text-lg">انتخاب فایل</span> یا کشیدن و رها کردن</p>
            <p class="text-xs text-gray-500 dark:text-gray-400">حداکثر حجم مجاز فایل 500 کیلو بایت می باشد</p>
        </Dropzone>
    </Label>
    <Label class="space-y-2">
        <span class="float-right">یادداشت</span>
    </Label>
    <Textarea class=""></Textarea>
    <Button type="submit" class="w-full1">بروز رسانی</Button>    
  </form>
</Modal>
