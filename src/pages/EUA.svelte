<script>
  import News from '../components/News.svelte';
  import Fetch from '../../hoc/Fetch.svelte';


  const props = {
    country: 'us'
  }
</script>

<Fetch { ...props } let:news>
  <News { news } />
</Fetch>