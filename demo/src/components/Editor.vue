<template>
    <div>
    <!--<input type="text" value="value" @input="updateValue($event.target.value)" /> -->
     <form @submit.prevent="addInfo">
         <input type="text" placeholder="add user info" v-model="usersInfo" />
     </form>
     <ul>
         <li v-for="(data,index) in info" :key="index">{{index}}.{{data.usersInfo}}
         </li>
     </ul>
    </div>
</template>

<script>
export default {
    name:"info",
    data(){
        return{
        usersInfo:"",
        info:[
        
      ]}
      
    },
    props: ['value'],

    methods:{
        updateValue(value){
            this.$emit('input', value);
        },
     addInfo(){
         this.info.push({usersInfo:this.usersInfo});
         this.usersİnfo='';

     }
    }
}
</script>