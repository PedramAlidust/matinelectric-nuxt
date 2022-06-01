<template>
        <!-- navigation section -->
    <nav class="navbar navbar-expand-lg py-3">
      <div class="container pe-5 pe-lg-0">
        <button
          class="nav-border pt-2 rounded"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navmenu"
        >
          <i class="bi-list h3"></i>
        </button>
        <div class="collapse navbar-collapse" id="navmenu">
          <ul class="navbar-nav pe-lg-3 p-0">
            <li v-for="menu_item in menu_data.slice().reverse()" :key="menu_item.id" class="nav-item ps-lg-2">
              <a :href="menu_item.acf.menu_link" class="nav-link active-item text-white">{{menu_item.acf.menu_title}}</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
</template>

<script>

export default {
  name: "TheHeader",
  props: ['menu_data']
};
</script>


<style scoped>

</style>
