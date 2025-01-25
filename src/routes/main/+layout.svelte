<div class="drawer lg:drawer-open">
  <input id="my-drawer-2" type="checkbox" class="drawer-toggle " />
  <div class="drawer-content flex flex-col">
    <!-- Page content here -->
    <label for="my-drawer-2" class="btn btn-neutral drawer-button lg:hidden">
      ☰
    </label>
    <slot /> <!-- Slot for page-specific content -->
  </div>
  <div class="drawer-side">
    <label for="my-drawer-2" aria-label="close sidebar" class="drawer-overlay"></label>
    <!-- Drawer Content -->
    <div class="flex flex-col justify-between min-h-full bg-base-200 text-base-content w-64">
      <!-- Sidebar Menu -->
      <ul class="menu p-4">
        <li><p class="font-normal text-base sm:text-lg md:text-xl lg:text-2xl xl:text-3xl">Turf Nation</p></li>
        
        <div class="divider"></div>
        <li><a href="dashboard">Turf Dashboard</a></li>
        <li><a href="freeze">Freeze Slots</a></li>
        <li><a href="revenue">Revenue Details</a></li>
      </ul>
      <!-- Login Button -->
      <div class="p-4 ">
        <a href="/login" class="btn btn-accent w-half">Logout</a>
      </div>
    </div>
  </div>
</div>

<style>
  a {
    font-family: 'Alexandria';
    font-weight: 200;
    font-size: 20px;
    margin: 5px;
  }
  p {
    font-family: 'Montserrat';
    font-weight: normal;
    font-size: 20px;
    margin: 5px;
  }

  .btn {
    border-radius: 5px;
    font-family: 'Montserrat';
    font-weight: normal;
  }
  
</style>
