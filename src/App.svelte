<script>
// @ts-nocheck

import TaskDetails from "./UserTasks/TaskDetails.svelte";
import TaskList from "./UserTasks/TaskList.svelte";

  
let isFav = null;
let tasks = [
      {
          id : "01",
          title : "حل تمرینات گرامر پیشرفته - درس سوم",
          dueDate : "1401/10/21",
          progress : "75%",
          isFav: !isFav
          
      },
      {
          id : "02",
          title : "تکمیل بخش احراز هویت پروژه وب شرکت فن پرداز داتیس",
          dueDate : "1401/10/24",
          progress : "45%",
          isFav: !isFav
          
      },
      {
          id : "03",
          title : "مرور لغات 1100 - بخش 12",
          dueDate : "1401/10/22",
          progress : "90%",
          isFav: !isFav
          
      },
      {
          id : "04",
          title : "گرامر پیشرفته ایلتس - صرف مجهول",
          dueDate : "1401/12/10",
          progress : "30%",
          isFav: !isFav
          
      }
      
  ]

</script>

<main>
    <TaskList {tasks}/>
   

</main>

<style>
  
</style>


