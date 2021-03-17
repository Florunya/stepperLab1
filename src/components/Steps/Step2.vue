<template>
    <div>
        <h2>Привет) Посмотри на картинки</h2>
            <v-img
                 :aspect-ratio="16/9"
                 :width="width"
                src="https://images.unsplash.com/photo-1512319302256-dc970e613e2c?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=3150&q=80"
            ></v-img>
            <v-img
                 :aspect-ratio="16/9"
                 :width="width"
                src="https://images.unsplash.com/photo-1475598322381-f1b499717dda?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1955&q=80"
            ></v-img>
            <v-img
                 :aspect-ratio="16/9"
                 :width="width"
                src="https://images.unsplash.com/photo-1495305730668-3d13ae2a3250?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&auto=format&fit=crop&w=1950&q=80"
            ></v-img>
         
       <v-btn @click="Accept()">Далее</v-btn>
    </div>
    
</template>

<script>
export default {
    name: 'Step2',
    methods:{
       Accept: function(){
            this.$emit('Accept')
            }
        }
}
</script>

<style scoped>
</style>