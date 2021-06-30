<!--<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>-->
<template>
  <div class="home">
    <h1>Home</h1>
    <input type="text" v-model="search">
    <p>search term - {{ search }}</p>
    <div v-for="name in matchingNames" :key="name">{{ name }}</div>
    <button @click="handleClick">stop watching</button>
  </div>
  <div>
    <input type="text" v-model="routedata.id">
    <button @click="goTo(routedata)">goTo</button>
  </div>

<!--    <About>
    <template v-slot:test>
      <a href="#">slot deneme</a>
      &lt;!&ndash;    <p>Hoşgeldin, {{username}}</p>&ndash;&gt;

    </template>
    <p>test paragraph to avoid fallback content</p>
  </About>-->

<!--  <Testlayout>
    <template v-slot:test>
      <p>Hoşgeldin, {{username}}</p>
      <a href="#">slot deneme</a>

    </template>
&lt;!&ndash;    <p>test paragraph to avoid fallback content</p>&ndash;&gt;
  </Testlayout>-->





</template>



<script>
import { computed, reactive, ref, watch, watchEffect } from 'vue'
//import About from "./About";
import Aboutme from "../components/Aboutme";
import Testlayout from "./Testlayout";
export default {
  name: 'Home',
  components: {Testlayout,Aboutme},
  methods:{
    goTo(routedata){
      console.log(routedata)
      this.$router.push({
        name:'Contact',
        params:{
          id:routedata.id
        }
      })
    }
  },
  setup() {
    //Data
    const search = ref('')
    const names = ref(['mario', 'yoshi', 'luigi', 'toad', 'bowser', 'koopa', 'peach'])
    const username = ref('Batuhan')
    const routedata = reactive({
      id:''
    })


    //Functions
    const matchingNames = computed(() => {
      return names.value.filter(name => name.includes(search.value))
    })

    const stopWatch = watch(search, () => {
      console.log('watch function ran')
    })
    const stopEffect = watchEffect(() => {
      console.log('watchEffect ran', search)
      //console.log(names.value)
    })
    const handleClick = () => {
      stopWatch()
      stopEffect()
    }

    const watchRoute = watch(routedata,()=>{
      console.log(routedata.id)
    })
    return {
      //Data//
      names,
      search,
      matchingNames,
      username,
      routedata,
      //Functions//
      handleClick }
  }

}
</script>