
<script>
    import Datepicker from "../Datepicker.svelte";
import Table from "./Table.svelte";
    import Collapse from "./collapse.svelte";
</script>
<div class="flex w-full flex-col p-4">
  <div class="card bg-base-300 rounded-box grid h-20 place-items-center">
    <h1>Freeze/Offline Bookings </h1>
  </div>
  <div class="divider"></div> 
</div>
<Collapse></Collapse>
<Datepicker></Datepicker>
<Table></Table>

<style>
    h1{
        font-family: 'Bebas Neue';
        font-size: 50px;
    }
    .divider{
    }
    
</style>