<script>
  import Logo from "./Logo.svelte";
  import NavMobile from "./NavMobile.svelte";
  let showMobileMenu = false;

  const openMenu = () => {
    showMobileMenu = true;
  };

  const closeMenu = () => {
    showMobileMenu = false;
  };
</script>

<style>
  .social-nav {
    display: flex;
    justify-content: flex-end;
    padding: 10px 5px 0;
  }

  .bottom-nav {
    background: var(--light-color);
  }

  .middle-nav {
    display: flex;
    justify-content: flex-end;
  }

  .below-nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 10px;
  }

  .buttons {
    display: flex;
  }

  .menu {
    display: flex;
  }

  li {
    padding-right: 30px;
  }

  .bed {
    width: 40px;
    padding-right: 10px;
    color: #fff;
  }

  .menu-button {
    display: none;
  }

  svg {
    width: 25px;
  }

  .phone-icon {
    display: none;
  }

  @media (max-width: 1000px) {
    .menu-button {
      display: block;
    }
    .menu {
      display: none;
    }
  }

  @media (max-width: 600px) {
    .btn {
      font-size: 12px;
      padding: 10px 20px;
    }

    .btn--primary {
      padding: 15px 30px;
    }

    .bed {
      width: 30px;
    }

    .phone {
      display: none;
    }

    .phone-icon {
      display: block;
    }
  }

  @media (max-width: 550px) {
    .buttons {
      flex-direction: column;
      gap: 10px;
    }
  }
</style>

<nav class="bottom-nav">
  <div class="middle-nav">
    <ul class="social-nav">
      <li class="phone-icon"><i class="fas fa-phone-alt" /></li>
      <li class="phone">819 838-4277</li>
      <li><i class="fab fa-facebook-f" /></li>
      <li><i class="far fa-envelope" /></li>
    </ul>
    <div class="menu-button" on:click={openMenu}>
      <svg viewBox="0 0 100 60" width="40" height="40">
        <rect width="100" height="10" />
        <rect y="30" width="100" height="10" />
        <rect y="60" width="100" height="10" />
      </svg>
    </div>
  </div>

  <ul class="below-nav">
    <Logo />
    <div class="menu">
      <li><a href=".">Restaurant</a></li>
      <li><a href=".">Pret-a-manger</a></li>
      <li><a href=".">Traiteur</a></li>
      <li><a href=".">Evenements</a></li>
      <li><a href=".">Promotions</a></li>
    </div>

    <div class="buttons">
      <button class="btn btn--secondary">
        <img src="./img/bed.png" class="bed" alt="" />
        Réserver</button>
      <button class="btn btn--primary">Commender ici</button>
    </div>
  </ul>
</nav>

<NavMobile show={showMobileMenu} {closeMenu} />
