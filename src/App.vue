<template>
  <!-- <Mymenu /> -->
   <!-- nicher moto kore open close kore likhle er vitor onno kicu o lekha jabe  -->
  <Mymenu> 
    <ul class="top-link">
                 <li v-for="mysingelmenu in mytopmenu"><a :href="mysingelmenu.url">{{ mysingelmenu.name }}</a></li>

								<!-- <li><a href="#">| About</a></li>
								<li><a href="#">| Contact</a></li>
								<li><a href="#">| Blog</a></li>
								<li><a href="#">| Service</a></li>						 -->
							</ul>

              <!-- main menu test  -->
              <!-- <div class="main-menu">
									<nav class="navigation">
										<ul class="nav menu">
											<li class="active"><a href="#">Home <i class="icofont-rounded-down"></i></a>
												<ul class="dropdown">
													<li><a href="index.html">Home Page 1</a></li>
												</ul>
											</li>
											<li><a href="#">Doctos </a></li>
											<li><a href="#">Services </a></li>
											<li><a href="#">Pages <i class="icofont-rounded-down"></i></a>
												<ul class="dropdown">
													<li><a href="404.html">404 Error</a></li>
												</ul>
											</li>
											<li><a href="#">Blogs <i class="icofont-rounded-down"></i></a>
												<ul class="dropdown">
													<li><a href="blog-single.html">Blog Details</a></li>
												</ul>
											</li>
											<li><a href="contact.html">Contact Us</a></li>
										</ul>
									</nav>
								</div> -->

  </Mymenu>
  <myslider @getinformation="receivedchildinfo" />
  <myschedule />
  <myfeature />
  <myfun />
  <mychoose />
  <mycalltoaction />
  <myportfolio />
  <myservice />
  <!-- <myprice price="500"/> -->
  <!-- <myprice v-bind:price="setprice"/> -->
  <!-- <myprice v-for="singelprice in setprice" v-bind:price="setprice"/> -->
  <!-- <myprice v-for="singelprice in setprice" v-bind:price="singelprice"/> -->
  <myprice v-for="singelprice in setprice" v-bind:price="setprice" />
  <myblog />
  <myclient />
  <myappointment />
  <mynewsletter />
  <!-- <myfooter class="footer" copyright="Nirob It Solutions"/> -->
  <!-- <myfooter style="background-color: red;" copyright="Nirob It Solutions"/> -->
  <myfooter @click="parentinfo" copyright="Nirob It Solutions" />

  <!-- class, style, v-on , we can pass -->

  {{ discount }}
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import TheWelcome from "./components/TheWelcome.vue";
import Mymenu from "./components/mymenu.vue";
import myslider from "./components/myslider.vue";
import myschedule from "./components/schedule.vue";
import myfeature from "./components/feature.vue";
import myfun from "./components/fun.vue";
import mychoose from "./components/choose.vue";
import mycalltoaction from "./components/calltoaction.vue";
import myportfolio from "./components/portfolio.vue";
import myservice from "./components/service.vue";
import myprice from "./components/price.vue";
import myblog from "./components/blog.vue";
import myclient from "./components/client.vue";
import myappointment from "./components/appointment.vue";
import mynewsletter from "./components/newsletter.vue";
import myfooter from "./components/footer.vue";

export default {
  name: "My Application",
  components: {
    Mymenu,
    myslider,
    myschedule,
    myfeature,
    myfun,
    mychoose,
    mycalltoaction,
    myportfolio,
    myservice,
    myprice,
    myblog,
    myclient,
    myappointment,
    mynewsletter,
    myfooter,
  },
  data() {
    return {
      cell: "01712345678",
      // setprice: 6020
      setprice: ["100", "200", "300", "400", "500"],
      discount: 0,
      mytopmenu: [
					{
						name: "About",
						url: "about"
					},
					{
						name: "Doctors",
						url: "doctors"
					},
					{
						name: "Contact",
						url: "contact"
					},
					{
						name: "FAQ",
						url: "faq"
					}
				]
    }
  },
  methods: {
    receivedchildinfo(getprice) {
      // alert("Allah is Mohan");
      // alert("Price is: "+getprice);
      if (getprice >= 300) {
        this.discount = 30;
      } else {
        this.discount = 10;
      }
    },
    parentinfo() {
      alert("This is parent info");
    },
  },
};
</script>

  <!-- <style>
  body {
    background-color: red;
  }
  </style> -->
