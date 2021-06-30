<template>

  <div class="aboutme">

    <h1>This is an about page</h1>



    <div>
      <button @click="testFunction"> Run testFunction </button>
    </div>
    <div>
      <button @click="test1"> Run test1 </button>
    </div>



<!--    <slot name="test"/>
    <slot name="default"/>-->

    <div>
      <slot name="default"> Fallback Content, by default (must be shown if no slot passed in)</slot><br/>
    </div>

    <div>
      <slot name="test">bunun yazdığını görüyorsam sıkıntı var, test isimli slottan içerik gelmeli</slot>
    </div>



    <div>
      <button @click="test2"> Run test2 </button>
    </div>
    <div>
      <button @click="test3"> Run test3 </button>
    </div>
  </div>
  {{ firstName }}

</template>

<script>

import Contact from "../views/Contact.vue";

export default {
  name: 'HelloWorld',
  props:{
    firstName:{type:String,default:'Batuhan'},
    lastName:{type:String,default:'Karahan'},
    phoneNumber:{type:String,default:'05305951743'},
    address:{type:String,default:'Altıntepe'}
  },
  components:{Contact},
  test:'testing you',
  context:{myname:'batuhankarahan'},

  setup(props, context){
    const testFunction = ()=>{
      console.log(Contact.context.somekey) // somevalue
    }
    const test1 = ()=>{
      console.log(Contact.context.testkey1) // testvalue1
      //console.log(context) // undefined

    }
    const test2 = ()=>{
      console.log(Contact.context.testkey2) // testvalue2
    }
    const test3 = ()=>{
      console.log(Contact.context.testkey3) // testvalue3
    }
    //console.log(Contact.context.)

    /*const{title}=toRefs(props)
    console.log(title)*/
    // Attributes (Non-reactive object)
    console.log(context.attrs)

    // Slots (Non-reactive object)
    console.log(context.slots)

    // Emit Events (Method)
    console.log(context.emit)

    console.log(context)

    /*let aboutme = {
      firstName:'Batuhan',
      lastName:'Karahan',
      phoneNumber:'05305951743',
      address:'Altıntepe'
    }*/

    return {
      //aboutme
      testFunction,
      test1,
      test2,
      test3
    }
  },
  /*methods:{
    sendInfoAboutMe(){
      this.$router.push(name:'Contact',params)// vue3 te context üzerinden erişiliyor (props,context)
    }
  }*/

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/*h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}*/
</style>
