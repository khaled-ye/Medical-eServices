<template>
    <div >
        <!-- <div>
            <b-navbar toggleable="lg" type="dark" variant="info">
                <b-navbar-brand href="#">Medical Services</b-navbar-brand>

                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

                <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav>
                    <router-link to='/pharmacie'>Pharmacies</router-link>
                    <router-link to='/hospital'>Hospitals</router-link>
                    <router-link to='/doctor'>Doctors</router-link>
                </b-navbar-nav>

                <b-navbar-nav>
                    <b-nav-item href="#">Pharmacies</b-nav-item>
                    <b-nav-item href="#">Hospitals</b-nav-item>
                    <b-nav-item href="#">Doctos</b-nav-item>
                </b-navbar-nav>

                Right aligned nav items
                <b-navbar-nav class="ml-auto">

                    <b-nav-item right>
                    Using 'button-content' slot
                    <template #button-content>
                        <em>Login</em>
                    </template>
                    </b-nav-item>
                </b-navbar-nav>
                </b-collapse>
            </b-navbar>
        </div> -->
        
        <b-container class="bv-example-row">
            <b-row class="justify-content-md-center">
                <b-col cols="12">
                    <!-- <h4>Welcome to our Medical Services</h4> -->
                    <div class="mt-4">
                        <b-carousel
                        id="carousel-1"
                        v-model="slide"
                        :interval="4000"
                        controls
                        indicators
                        background="#ababab"
                        img-width="1024"
                        img-height="480"
                        style="text-shadow: 1px 1px 2px #333;"
                        @sliding-start="onSlideStart"
                        @sliding-end="onSlideEnd"
                        >
                        <!-- Text slides with image -->
                            <!-- caption="First slide"
                            text="Nulla vitae elit libero, a pharetra augue mollis interdum." -->
                        <b-carousel-slide v-bind:img-src="require('.././assets/pharmacie.png')">
                            <h1>Pharmacies</h1>
                        </b-carousel-slide>

                        <!-- Slides with custom text -->
                        <b-carousel-slide v-bind:img-src="require('.././assets/hospital.png')">
                            <h1>Hospitals</h1>
                        </b-carousel-slide>

                        <!-- Slides with image only -->
                        <b-carousel-slide v-bind:img-src="require('.././assets/doctor.png')">
                            <h1>Doctors</h1>
                        </b-carousel-slide>

                        <!-- Slides with img slot -->
                        <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
                        <!-- <b-carousel-slide>
                            <template #img>
                            <img
                                class="d-block img-fluid w-100"
                                width="1024"
                                height="480"
                                src="https://picsum.photos/1024/480/?image=55"
                                alt="image slot"
                            >
                            </template>
                        </b-carousel-slide> -->

                        <!-- Slide with blank fluid image to maintain slide aspect ratio -->
                        <!-- <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image">
                            <p>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eros felis, tincidunt
                            a tincidunt eget, convallis vel est. Ut pellentesque ut lacus vel interdum.
                            </p>
                        </b-carousel-slide> -->
                        </b-carousel>

                        <!-- <p class="mt-4">
                        Slide #: {{ slide }}<br>
                        Sliding: {{ sliding }}
                        </p> -->
                    </div>
                </b-col>
            </b-row>
        </b-container>
        <router-view/>
    </div>
    
</template>

<script>
export default {
    name: 'Home',
    components: {

    },
    data() {
      return {
        slide: 0,
        sliding: null
      }
    },
    methods: {
      onSlideStart(slide) {
        console.log(slide)
        this.sliding = true
      },
      onSlideEnd(slide) {
        console.log(slide)
        this.sliding = false
      }
    }
}
</script>

<style>

</style>