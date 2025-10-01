

<template>
<Mymenu/>
<myslider @getinformation="receivedchildinfo"/>
<myschedule/>
<myfeature/>
<myfun/>
<mychoose/>
<mycalltoaction/>
<myportfolio/>
<myservice/>
<!-- <myprice price="500"/> -->
<!-- <myprice v-bind:price="setprice"/> -->
<!-- <myprice v-for="singelprice in setprice" v-bind:price="setprice"/> -->
<!-- <myprice v-for="singelprice in setprice" v-bind:price="singelprice"/> -->
<myprice v-for="singelprice in setprice" v-bind:price="setprice"/>
<myblog/>
<myclient/>
<myappointment/>
<mynewsletter/>
<myfooter copyright="Nirob It Solutions"/>
{{ discount }}
</template>

<script >
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import Mymenu from './components/mymenu.vue';
import myslider   from './components/myslider.vue';
import myschedule from './components/schedule.vue';
import myfeature from './components/feature.vue';
import myfun from './components/fun.vue';
import mychoose from './components/choose.vue';
import mycalltoaction from './components/calltoaction.vue';
import myportfolio from './components/portfolio.vue';
import myservice from './components/service.vue';
import myprice from './components/price.vue';
import myblog from './components/blog.vue';
import myclient from './components/client.vue';
import myappointment from './components/appointment.vue';
import mynewsletter from './components/newsletter.vue';
import myfooter from './components/footer.vue';

export default{
    name: 'My Application',
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
      myfooter
    },
    data(){
      return{
        cell: "01712345678",
        // setprice: 6020
        setprice: ['100','200','300','400','500'],
        discount:0,
      }
    },
    methods:{
      receivedchildinfo(getprice){
        // alert("Allah is Mohan");
        // alert("Price is: "+getprice);
        if(getprice>=300){
          this.discount=30;
      }else
      {
        this.discount=10;
      }
      }
    }
}
</script>
