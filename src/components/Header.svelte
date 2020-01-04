<script>
  import Link from './Link.svelte';
</script>

<header>
  <div class='header'>
    <div class='menu'>
      <div class='sub-menu'>
        <ul>
          <li>
            <Link page={{ path: '/', name: 'Brasil' }} />
          </li>
          <li>
            <Link page={{ path: '/eua', name: 'EUA' }} />
          </li>
        </ul>
      </div>
    </div>
  </div>
</header>

<style>
  .header {
    display: flex;
    flex-direction: column;
    width: 100%;

    top: 0;
    align-items: center;
    text-align: center;
  }
  .menu {
    display: inline-block;
    width: 100%;
    padding: 5px 0px;

    background-color: #ffffff;
  }
  .sub-menu {
    display: flex;
    justify-content: space-between;
  }
  ul {
    margin: 0px;
    padding: 0px;
    overflow: hidden;

    list-style-type: none;
    margin-left: 0.5rem;
  }
  li {
    position: relative;
    float: left;
    font-size: 17px;

    font-weight: bold;
  }
  li:nth-child(2n)::before {
    position: absolute;
    width: 2px;
    height: 18px;

    content: "";
    background-color: #dedede;
    left: 0px;
  }
</style>
