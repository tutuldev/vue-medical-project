

<template>
<Mymenu/>
<myslider/>
<myschedule/>
<myfeature/>
<myfun/>
<mychoose/>
<mycalltoaction/>
<myportfolio/>
<myservice/>
<myprice/>
<myblog/>
<myclient/>
<myappointment/>
<mynewsletter/>
<myfooter/>
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
    }
}
</script>
