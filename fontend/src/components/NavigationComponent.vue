<script>
export default {
    name: "NavigationComponent",
    methods: {
      logout(){
        // TODO : Supprimer les cookies de connexion
        this.$router.push('/');
      }
    },
};
</script>

<template>
    <Header class="mainHeader">
        <div class="wrapper">
            <p class="title">
              <router-link to="/home" class="navigation-link">
                ClassBooking
              </router-link>
            </p>
            <ul class="navigation-list">
                <li class="navigation-item">
                    <router-link to="/home" class="navigation-link"
                        >Les salles</router-link
                    >
                </li>
                <li class="navigation-item">
                    <router-link to="/home" class="navigation-link"
                        >Le calendrier</router-link
                    >
                </li>
                <li class="navigation-item">
                    <router-link to="/home" class="navigation-link"
                        >Mon espace</router-link
                    >
                </li>

                <!-- 
                TODO : A afficher si admin

                <li class="navigation-item">
                  <router-link to="/home" class="navigation-link">Administration</router-link>
                </li> -->

                <li class="navigation-item">
                  <button @click="logout" class="btn-logout btn-style-2">Se déconnecter</button>
                </li>
            </ul>
        </div>
    </Header>
</template>

<style scoped lang="scss">
  .mainHeader{
    background: var(--color-1);
  }
  .wrapper{
    width: 100%;
    max-width: 140rem;
    height: 8rem;
    padding-left: 3rem;
    padding-right: 3rem;

    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin-left: auto;
    margin: auto;
  }
  .title{
    font-family: var(--font-1);
    font-size: 3rem;
    font-weight: 700;
    text-transform: uppercase;
    color: #fff;
  }
  .navigation{
    &-list{
      display: flex;
      align-items: center;
      gap: 3rem;
    }
    &-item{
      font-family: var(--font-1);
      font-size: 2rem;
    }
    &-link{
      text-decoration: none;
      color: #eee;
      transition: .2s;

      &:hover{
        color: #fff;
      }
    }
  }

  .btn-logout{
    padding: .5rem 1.5rem;
  }
</style>
