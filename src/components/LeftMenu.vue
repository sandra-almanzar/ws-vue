<template>
  <div class="d-flex flex-column collapsed border-right">
    <ul class="nav mt-2 flex-column">
      <li
        v-for="(itemLeft, index) in leftMenu"
        :key="index"
        class="nav-item position-relative"
      >
        <a href="#" class="nav-link active">
          <i :class="itemLeft.icono" class="bi-3x mx-2 icono d-block"> </i>
          <span class="text-dark fw-bold item pt-0.5em text-truncate">{{
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
  width: "10px", height= "10px";
  color: black;
}
.item {
  font-size: 10.5px;
}
</style>
