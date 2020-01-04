<script>
  import { onMount } from 'svelte';
  import { apiKey } from '../config/config'

  export let country = 'br'
  export let news = [];

  async function getNews() {
    const res = await fetch(`https://newsapi.org/v2/top-headlines?country=${country}&apiKey=${apiKey}`)
    const json = await res.json();
    news = json.articles;
  }

  onMount(getNews)
</script>

<slot {news} />