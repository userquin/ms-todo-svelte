<script lang="ts">
  import TasksList from '$components/Task/TasksList.svelte';
  import type { List } from '$stores/lists.store';
  import Wallpaper from '../Wallpaper.svelte';
  import ListViewHeader from './ListViewHeader.svelte';

  export let list: List;
  export let listID: string;
</script>

<svelte:head>
  <title>{list.title} - Beautiful Todo</title>
</svelte:head>

<Wallpaper {list} />

<section class="container">
  <ListViewHeader {listID} />

  <TasksList {listID} />
</section>

<style lang="scss">
  .container {
    padding: 1rem 2rem;
  }
</style>
