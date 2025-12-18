<script lang="ts">
  import { Catppuccin } from '../color.js';
  
  let count: number = $state(0)
  const increment = () => {
    count += 1
  }
</script>

<button onclick={increment} style="background-color: {Catppuccin.Mantle}; color: {Catppuccin.Text}; border-color: {Catppuccin.Surface0};">
  count is {count}
</button>
