<template>
  <div class="TrySalesBtn">
    <button class="navButtons" id="salesBtn">TALK TO SALES</button>
    <button class="navButtons" id="tryBtn">TRY FOR FREE</button>
  </div>
</template>
<script>
export default {
  name: "TrySalesBtn",
};
</script>
<style>
.TrySalesBtn {
  display: flex;
  justify-content: space-evenly;
  width: 80%;
  height: auto;
}
.TrySalesBtn button {
  padding: 8px 12px;
  border: 2px solid #f4ede4;
  border-radius: 5px;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-weight: 600;
}
.TrySalesBtn button:hover {
  transform: scale(1.02);
}
.TrySalesBtn #salesBtn {
  background-color: rgb(116, 1, 116);
  color: #f4ede4;
}
.TrySalesBtn #tryBtn {
  color: rgb(116, 1, 116);
  background-color: #f4ede4;
}
@media screen and (max-width: 767px) {
  .TrySalesBtn .navButtons {
    font-size: calc(0.875rem + (0 * (100vw - 400px) / 624));
    padding-left: calc(0.975rem + (0 * (100vw - 400px) / 624));
    padding-right: calc(0.975rem + (0 * (100vw - 400px) / 624));
    padding-top: calc(0.675rem + (0 * (100vw - 400px) / 624));
    padding-bottom: calc(0.675rem + (0 * (100vw - 400px) / 624));
  }
}
</style>
