<template>
  <div class="contact">
    <h1>This is a contact page</h1>
    <p>{{n}}</p>
  </div>
  <p> User id : {{routeParamVal}}</p>
<!--  <About/>-->
</template>
<script>
//import About from "./About";
import Aboutme from "../components/Aboutme";
import {onMounted, ref} from "vue";
import {useRoute} from 'vue-router';
export default {
  components: {Aboutme},//{About},
  context:{
    somekey:'somevalue',
    testkey1:'testvalue1',
    testkey2:'testvalue2',
    testkey3:'testvalue3',
  },
  setup(props,context){
    /*const n = About.context.myname
    console.log(About.context.myname)*/
    const n = Aboutme.context.myname
    const routeParamVal = ref('default value')
    const route = useRoute()

    onMounted( () => {
      console.log(route)
      routeParamVal.value = route.params.id //context.root.$route.params.id  //outdated

      //console.log(context.root.$route)
      console.log(routeParamVal.value)
    })


    console.log(Aboutme.context.myname)
    return{
      n,
      routeParamVal
    }
  }
}
</script>