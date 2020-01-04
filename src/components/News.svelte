<script>
  export let news;
</script>

<div class='container'>
  {#each news as item}
  <article class='wrapper'>
    <a href={ item.url } target='_blank'>
      <figure class='figure-right'>
        <img src={ item.urlToImage } alt="news" />
      </figure>
      <footer class='article-info'>
        <span>{ item.source.name || '' }</span>
        <h2 class='article-title'>
          { item.title }
        </h2>
      </footer>
    </a>
  </article>
  {/each}
</div>

<style>
  .container {
    display: block;
  }
  .wrapper {
    margin-bottom: 1.5rem;
  }
  .figure-right {
    height: 202px;
  }
  img {
    width: 100%;
    height: 100%;
  }
  .article-info {
    margin-left: 20px;
    margin-right: 20px;
  }
  .article-title {
    margin-bottom: 0;
    margin-top: 0.5rem;
    font-family: 'Roboto', sans-serif;
    font-size: 18px;
    line-height: 1.11;
    color: #242425;
  }
  span {
    font-size: 13px;
    font-family: 'Roboto', sans-serif;
    color: #e11b22;
  }
  figure {
    margin-left: 20px;
    margin-right: 20px;
  }
  a {
    text-decoration: none;
  }
  @media screen and (min-width: 800px) {
    .container {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr 1fr;
    }
  }
</style>