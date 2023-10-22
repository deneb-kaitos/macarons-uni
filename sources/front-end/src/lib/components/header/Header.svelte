<script>
  export const prerender = true;

  const links = {
    home: {
      title: 'home',
      href: '/',
    },
    contacts: {
      title: 'contacts',
      href: '/contacts',
    },
    login: {
      title: 'login',
      href: '/login',
    },
    account: {
      title: 'account',
      href: '/account',
    },
  };

  let isAuthenticated = false;
</script>

<style>
  header {
    grid-area: app-header;
    position: sticky;
    top: 0;
    display: flex;
    justify-content: flex-end;
    align-items: stretch;
    font-variant: all-petite-caps;
    height: 5rem;
    z-index: 1;

    & nav {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 0.25rem;
    
      & a {
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        padding: 0 1rem;
      }
    }
  }
</style>
<header>
  <nav>
    <a href="/">home</a>
    <a href="/contacts">contacts</a>
    <a href="{ isAuthenticated === true ? links.account.href : links.login.href }">{ isAuthenticated === true ? links.account.title : links.login.title }</a>
  </nav>
</header>