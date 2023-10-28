<template>
  <nav class="sticky-top">
    <div class="bg-dark color-white" style= "position: sticky; top: 0; z-index: 1;" >
        Free Shipping on orders over $50
      </div>
  </nav>
  <nav class="navbar navbar-expand-lg bg-light top mt-4" style= "position: fixed; top: 0; left: 0; right: 0; z-index: 1;">
    
    <div>
      <a class="navbar-brand mr-auto pl-3" href="#"
        style="color: #333; font-weight: bold; font-family: 'Oxygen-Bold'; font-size: 2em;">PISTONS</a>
    </div>
      <div class="collapse navbar-collapse" id="navbarNavDropdown">
        <ul class="navbar-nav mx-auto">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#"
              style="color: #333; font-weight: bold; font-family: 'Oxygen-Bold';">NEW</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#" style="color: #333; font-weight: bold; font-family: 'Oxygen-Bold';">BRANDS</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#"
              style="color: #333; font-weight: bold; font-family: 'Oxygen-Bold';">COLLECTIONS</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#"
              style="color: #333; font-weight: bold; font-family: 'Oxygen-Bold';">ACCESSORIES</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#" style="color: #333; font-weight: bold; font-family: 'Oxygen-Bold';">ABOUT</a>
          </li>
        </ul>
      </div>
      <div style="display: inline-block">
          <div class="navbar-nav ml-auto deepan">
          
            <a  class ="m-2 mr-1" href="#" style="color: #333; font-weight: bold; font-family: 'Oxygen-Bold';">
              <i class="fas fa-shopping-cart"></i>
            </a>
          
            <a  class ="toggle m-2 ml-1" @click="searchVisible = true" style="color: #333; font-weight: bold; font-family: 'Oxygen-Bold';">
              <i class="fas fa-search"></i>
            </a>
          <button class="toggle ml-auto d-lg-none" @click="drawerVisible = true">
            <span class="navbar-toggler-icon"></span>
          </button>
        </div>
      </div>
      
    <!-- </div> -->
  </nav>
  <div
    class="right-drawer bg-light" 
    :style="{
      width: drawerVisible ? '25vw' : '0',
      paddingLeft: drawerVisible ? '10px' : '0',
    }"
  >
    <div style="text-align: right; margin: 5px">
      <button class="close" @click="drawerVisible = false">&#9587;</button>
    </div>
    <h4>NEW</h4>
    <h4>BRANDS</h4>
    <h4>COLLECTIONS</h4>
    <h4>ACCESSORIES</h4>
    <h4>ABOUT</h4>
  </div>
  
  <div
    class="drawer-mask"
    :style="{
      width: drawerVisible ? '100vw' : '0',
      opacity: drawerVisible ? '0.6' : '0',
    }"
    @click="drawerVisible = false"
  ></div>
  /////////////////////////////////
  <div
      class="search-drawer bg-light" 
      :style="{
        width: searchVisible ? '25vw' : '0',
        paddingLeft: searchVisible ? '10px' : '0',
      }"
    >
      <div style="text-align: right; margin: 5px">
        <button class="close" @click="searchVisible = false">&#9587;</button>
      </div>
      <form>
              <input type="text" placeholder="Search...">
              <button type="submit">Search</button>
      </form>
    </div>
  
    <div
      class="drawer-mask"
      :style="{
        width: searchVisible ? '100vw' : '0',
        opacity: searchVisible ? '0.6' : '0',
      }"
      @click="searchVisible = false"
    ></div> 

  <!-- <div class="right-drawer" :style="{ width: searchVisible ? '100%' : '0' }">
        <div class="drawer-mask" v-if="searchVisible" @click="searchVisible = false"></div>
        <div class="drawer-content">
          <form>
            <input type="text" placeholder="Search...">
            <button type="submit">Search</button>
          </form>
        </div>
      </div> -->
</template>

<script>
/* eslint-disable */
export default {
  name: "Nav",
  data() {
    return {
      drawerVisible: false,
      searchVisible: false,
    };
  },
};

</script>

<style scoped>

.deepan{
  display: inline-block;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.search-drawer {
  position: fixed;
  top: 0;
  right: 0;
  width: 0;
  overflow: hidden;
  margin-top: 10vh;
  height: 10%;
  padding-top: 3vh;
  padding-left: 1;
  border-left: 1px solid whitesmoke;
  background: white;
  z-index: 200;
  transition: all 0.2s;
}
.right-drawer {
  position: fixed;
  top: 0;
  right: 0;
  width: 0;
  overflow: hidden;
  margin-top: 10vh;
  height: 30vh;
  padding-top: 6vh;
  padding-left: 1;
  border-left: 1px solid whitesmoke;
  background: white;
  z-index: 200;
  transition: all 0.2s;
}
.drawer-mask {
  position: fixed;
  left: 0;
  top: 0;
  width: 0;
  height: 100vh;
  background: #000;
  opacity: 0.3;
  z-index: 199;
  transition: opacity 0.2s;
}
.drawer-content {
  padding: 1rem;
}
</style>
