<script>
  import { onDestroy } from 'svelte';
  import { curRoute } from '../store';

  import router from '../router/router';

  let component;

  const unsubscribe = curRoute.subscribe(value => {
    component = router.filter(r => r.path === $curRoute)[0].component;
  })

  onDestroy(unsubscribe);
</script>

<div>
  <svelte:component this={ component } />
</div>

<style>
</style>