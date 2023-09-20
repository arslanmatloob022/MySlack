<template>
  <div class="TrySalesBtn">
    <button class="navButtons" id="salesBtn">TALK TO US</button>
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
  width: 100%;
  height: auto;
}
.TrySalesBtn button {
  padding: 8px 18px;
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
@media screen and (max-width: 667px) {
  .TrySalesBtn button {
    font-size: calc(3px + 1vw);
    padding-left: calc(28px + 1vw);
    padding-right: calc(28px + 1vw);
    width: 160px;
  }
}
</style>
