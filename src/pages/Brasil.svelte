<script>
  import News from '../components/News.svelte';
  import Fetch from '../../hoc/Fetch.svelte';


  const props = {
    country: 'br'
  }
</script>

<Fetch { ...props } let:news>
  <News { news } />
</Fetch>
