<template>
  <div class="dropdown-menu" v-show="isOpen" @mouseleave="closeMenu">
    <ul>
      <li v-for="item in menuItems" :key="item.id">
        <a :href="item.link">{{ item.label }}</a>
        <p>{{ item.description }}</p>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isOpen: false,
      menuItems: [
        { id: 1, label: "Item 1", link: "#", description: "Items description" },
        { id: 2, label: "Item 2", link: "#", description: "Items description" },
        { id: 3, label: "Item 2", link: "#", description: "Items description" },
        { id: 4, label: "Item 2", link: "#", description: "Items description" },
      ],
    };
  },
  methods: {
    openMenu() {
      this.isOpen = true;
    },
    closeMenu() {
      this.isOpen = false;
    },
  },
};
</script>
<style>
.dropdown-menu {
  background-color: aliceblue;
  z-index: 1000;
}

.dropdown-menu ul li a {
  font-size: large;
  color: black;
}
</style>
