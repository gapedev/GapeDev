<script>
  export let width;
  export let height;
  export let fill = "currentColor";
  export let d;
  export let iconClass;
</script>

<svg class={iconClass} {width} {height} viewBox="0 0 24 24">
  <path {d} {fill} />
</svg>
