<template>
    <div>
            <h1>Заполните ваши данные :</h1>

            <p class="Error">{{Error}}</p>
            
            <v-text-field class="vInput"
                v-model="FirstName"
                label="Имя"
                placeholder="">
            </v-text-field>
            <v-text-field class="vInput"
                v-model="LastName"
                label="Фамилия"
                placeholder="">
            </v-text-field>
            <v-btn @click="Accept()">Далее</v-btn>
            
    </div>
</template>
 
<script>
export default {
    name: 'Step1',
    data: function(){
        return{
            FirstName: "",
            LastName: "",
            Error: ""
        }
    },
    methods:{
        Accept: function(){
            if((this.FirstName == "")||(this.LastName == ""))
                this.Error = "Заполните все поля"
            else{
                this.Error = "",
                this.$emit('Accept',this.FirstName, this.LastName)
            }
        }
    }
}
</script>

<style scoped>
.vInput{
    width: 50%;
}
.Error{
    color: rgb(255, 0, 0);
}
#fon{
    background-color: blueviolet;
}

</style>