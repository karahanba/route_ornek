<template>
<!--
//this part has moved to Aboutme.vue
  <div class="about">

    <h1>This is an about page</h1>



    <div>
      <button @click="testFunction"> Run testFunction </button>
    </div>
    <div>
      <button @click="test1"> Run test1 </button>
    </div>

    <div>
      <slot name="default"> Fallback Content, by default (must be shown if no slot passed in)</slot><br/>
      <slot name="test">ddddaddd</slot>
    </div>
    <div>
      <button @click="test2"> Run test2 </button>
    </div>
    <div>
      <button @click="test2"> Run test3 </button>
    </div>
  </div>
  {{ firstName }}-->
  <Aboutme>
    <template v-slot:test>
      <a href="#">test slot deneme</a>
      <p>merhaba</p>
    </template>
  </Aboutme>
</template>

<script>
import Aboutme from '../components/Aboutme.vue'

import {renderSlot, toRefs} from 'vue'
//import Contact from "./Contact";

export default {
  name:'About',
  //moved props,test object and context to Aboutme.vue
  components:{Aboutme},

 /* setup(props, context){
    const testFunction = ()=>{
      console.log(Contact.context.somekey)
    }
    const test1 = ()=>{
      //console.log(Contact.context.testkey1)
      console.log(context)

    }
    const test2 = ()=>{
      //console.log(Contact.context.testkey2)
    }
    const test3 = ()=>{
      //console.log(Contact.context.testkey3)
    }
    //console.log(Contact.context.)

    /!*const{title}=toRefs(props)
    console.log(title)*!/
    // Attributes (Non-reactive object)
    console.log(context.attrs)

    // Slots (Non-reactive object)
    console.log(context.slots)

    // Emit Events (Method)
    console.log(context.emit)

    console.log(context)

    /!*let aboutme = {
      firstName:'Batuhan',
      lastName:'Karahan',
      phoneNumber:'05305951743',
      address:'Altıntepe'
    }*!/

    return {
      //aboutme
      testFunction,
      test1,
      test2,
      test3
    }
  },*/
  /*methods:{
    sendInfoAboutMe(){
      this.$router.push(name:'Contact',params)// vue3 te context üzerinden erişiliyor (props,context)
    }
  }*/
}
</script>

<style scoped>

</style>