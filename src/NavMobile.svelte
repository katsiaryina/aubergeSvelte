<script>
  import { fade, fly } from "svelte/transition";
  import Logo from "./Logo.svelte";

  export let show;
  export let closeMenu;
</script>

<style>
  div {
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: var(--dark-color);
    color: var(--pale-color);
    display: flex;
    flex-direction: column;
    justify-content: top;
    align-items: center;
    padding: 60px;
    z-index: 10;
    text-align: center;
  }

  li {
    /* margin-bottom: 20px; */
    border-bottom: 1px dashed rgba(250, 250, 250, 0.2);
    padding: 15px 0;
  }

  li:first-of-type,
  li:last-of-type {
    border-bottom: none;
  }

  a {
    width: 100%;
    display: block;
  }
  button {
    border-radius: 40px;
    padding: 10px 30px;
    justify-self: flex-end;
    align-self: flex-end;
    margin-bottom: 20px;
  }
</style>

{#if show}
  <div in:fly={{ y: -200, duration: 600 }} out:fade>
    <button on:click={closeMenu} class="btn btn--secondary"> X </button>
    <ul>
      <li>
        <a href="."><Logo /></a>
      </li>
      <li><a href=".">Restaurant</a></li>
      <li><a href=".">Pret-a-manger</a></li>
      <li><a href=".">Traiteur</a></li>
      <li><a href=".">Evenements</a></li>
      <li><a href=".">Promotions</a></li>
    </ul>
  </div>
{/if}
