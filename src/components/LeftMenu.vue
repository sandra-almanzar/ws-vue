<template>
  <div class="d-flex flex-column align-items-center collapsed border-right">
    <ul class="nav mt-2 flex-column">
      <li
        v-for="(itemLeft, index) in leftMenu"
        :key="index"
        class="nav-item position-relative"
      >
        <a href="#" class="nav-link active">
          <i :class="itemLeft.icono" class="icono d-block"> </i>
          <span class="text-black fw-bold item text-truncate">{{
            itemLeft.nombre
          }}</span>
        </a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "left-menu",
  props: { leftMenu: Array },
};
</script>
<style>
.icono {
  color: black;
}
.item {
  font-size: 10.5px;
}
</style>
