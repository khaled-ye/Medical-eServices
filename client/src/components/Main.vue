<template>
  <div class="main">
      <div>
        <b-navbar toggleable="lg" type="dark" variant="info">
            <b-navbar-brand href="#">Medical Services</b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>

            <b-navbar-nav class="navLink">
                <router-link to='/'>Home</router-link>
                <router-link to='/pharmacie'>Pharmacies</router-link>
                <router-link to='/hospital'>Hospitals</router-link>
                <router-link to='/doctor'>Doctors</router-link>
            </b-navbar-nav>
            

            <!-- <b-navbar-nav>
                <b-nav-item href="#">Pharmacies</b-nav-item>
                <b-nav-item href="#">Hospitals</b-nav-item>
                <b-nav-item href="#">Doctors</b-nav-item>
            </b-navbar-nav> -->

            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto navLink">
                <!-- <b-nav-form>
                  <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
                  <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
                </b-nav-form> -->
            
                <router-link to='/login'>Login</router-link>

                <!-- <b-nav-item-dropdown right> -->
                <!-- Using 'button-content' slot -->
                <!-- <template #button-content>
                    <em>User</em>
                </template>
                <b-dropdown-item href="#">Sign Out</b-dropdown-item>
                </b-nav-item-dropdown> -->
            </b-navbar-nav>
            </b-collapse>
        </b-navbar>
        
      </div>
      <router-view/>
   
  </div>
</template>

<script>


export default {
  name: 'main',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.navLink a {
  padding: 0 10px;
  color: white;
  /* font-weight: bold; */
}
</style>
