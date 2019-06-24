<template>
  <div id="app">
    <div id="nav-wide" class="fixed-nav-bar">
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
    <router-view id="page-content"/>
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
  overflow: hidden;
  // max-width: $max-width;
  // margin: 0 $margin;
}
#page-content {
  margin: 120px 10vw;
  text-align: center;
  // display: inline-block;
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
.fixed-nav-bar {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 9999;
  width: 100%;
  background-color: #ffffff;
  // 78A93B
  // background-color: #5c415d;
  // background: rgba(92, 65, 93, 0.97);
  // background: rgba(255, 255, 255, 0.97);
  backdrop-filter: blur(10px);
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
    transition: all 2.4s ease-out;
    -webkit-transition: all 0.4s ease-out;
    color: #6f6f6f;
    &.router-link-exact-active {
      color: #038194;
    }
  }

  a:hover {
    color: black;
    text-shadow: 2px 4px 6px rgba(0, 0, 0, 0.13);
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
      padding-right: 12px;
    }

    .text {
      text-transform: capitalize;
      font-weight: normal;
      font-size: 14px;
    }
  }
}
</style>
