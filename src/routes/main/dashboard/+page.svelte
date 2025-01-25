<script>
    import Table from "./Table.svelte";
    import Datepicker from "../Datepicker.svelte";
    import Info from "./Info.svelte";
</script>

<div class="flex w-full flex-col p-4">
    <div class="relative flex items-center bg-base-300 rounded-box h-20 p-4">
      <!-- Turf Name -->
      <h2 class="absolute right-4 text-xl font-medium">Mihir Yadav</h2>
      <!-- Dashboard Title -->
      <h1 class="mx-auto text-3xl">Dashboard</h1>
    </div>
    <br>
  </div>

<Datepicker></Datepicker>
<Info></Info>
<Table></Table>

<style>
    h1 {
        font-family: 'Bebas Neue';
        font-size: 50px;
    }
    h2 {
        font-family: 'Montserrat';
        font-size: 15px;
        text-align: left; /* Aligns the text to the left */
        margin: 0;
    }
    h3{
        font-family: 'Montserrat';
        font-size: 15px;
    }
</style>
