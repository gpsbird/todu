<template>
  <label :class="['pretty-checkbox', {'checked': checked}]">
    <span class="icon-checked"></span>
  </label>
</template>

<script>
export default {
  props: {
    checked: Boolean,
  }
}
</script>

<style>
.pretty-checkbox {
  display: inline-block;
  vertical-align: middle;
  margin-top: 2px;
  margin-right: 8px;
  width: 16px;
  height: 16px;
  color: hsl(166, 60%, 40%);
  border: 2px solid;
  border-radius: 6px;
  cursor: pointer;
}
.pretty-checkbox .icon-checked {
  display: block;
  width: 0;
  height: 100%;
  overflow: hidden;
  transition: width ease-in 0.2s;
}
.pretty-checkbox .icon-checked:before {
  content: '';
  margin-top: 3px;
  margin-left: 2px;
  display: block;
  width: 10px;
  height: 5px;
  border-left: 2px solid;
  border-bottom: 2px solid;
  transform: rotate(-45deg);
}
.pretty-checkbox.checked .icon-checked {
  width: 100%;
}
</style>
