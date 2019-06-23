<template>
  <div id="app">
    <div id="nav-wide">
      <nav>
        <div id="nav-content">
          <router-link to="/">HOME</router-link>
          <div class="links">
            <router-link to="/design">design</router-link>
            <router-link to="/development">development</router-link>
            <router-link to="/web3">web3</router-link>
            <router-link to="/music">music</router-link>
          </div>
          <div class="profile">
            <img class="pic" src="https://i.imgur.com/L9rLNo7.png">
            <div class="text">Jeremy Stern</div>
          </div>
        </div>
      </nav>
    </div>
    <router-view/>
  </div>
</template>



<style lang="scss">
@import "/styles/global.scss";
@import "/styles/buttons.scss";
$max-width: 1152px;
$margin: 75px;

#app {
  font-family: "Avenir Next", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  // overflow: hidden;
  // max-width: $max-width;
  // margin: 0 $margin;
  // color: #2c3e50;
}
#nav-wide {
  width: 500%;
  margin-left: -200%;
  border-bottom: 2px solid rgba(196, 196, 196, 0.25);
}
#nav-content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 75vw;
}
nav {
  display: inline-block;
  height: 90px;
  line-height: 90px;
  max-width: $max-width;

  .links {
    font-size: 14px;
    font-variant: small-caps;
    color: #6f6f6f;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    flex-grow: 0.4;
  }

  a {
    // font-weight: bold;
    color: #6f6f6f;
    &.router-link-exact-active {
      color: #038194;
    }
  }

  a:hover {
    color: black;
  }

  .profile {
    display: flex;
    flex-direction: row;

    .pic {
      // box-shadow: 2px 4px 7px rgba(0, 0, 0, 0.1);
      border-radius: 50%;
      width: 30px;
      height: 30px;
      margin: auto;
      padding-right: 5px;
    }

    .text {
      text-transform: capitalize;
      font-weight: normal;
      font-size: 14px;
    }
  }
}
</style>
