<template>
    <div>
        <v-stepper v-model="numStep">
            <v-stepper-header>
                <v-stepper-step :complete="numStep > 1" step="1">
                     Назовись
                </v-stepper-step>
                 <v-divider></v-divider>
                <v-stepper-step :complete="numStep > 2" step="2">
                    Насладись
                </v-stepper-step>
                 <v-divider></v-divider>
                <v-stepper-step :complete="numStep > 3" step="3">
                    Пока
                </v-stepper-step>
                
            </v-stepper-header>
            <v-stepper-items>
                <v-stepper-content step="1">
                    <v-card  class="card"
                        elevation="10">
                        <Step1  @Accept="AcceptName"/>
                    </v-card>
                </v-stepper-content>
                <v-stepper-content step="2">
                    <v-card  class="card"
                        elevation="10">
                        <Step2  @Accept="next"/>
                    </v-card>
                </v-stepper-content>
                <v-stepper-content step="3">
                    <v-card  class="card"
                        elevation="10">
                        <Step3  :Person="Person"/>
                    </v-card>
                </v-stepper-content>
            </v-stepper-items>
        </v-stepper>
    </div>    
</template>

<script>
import Step1 from './Steps/Step1.vue'
import Step2 from './Steps/Step2.vue'
import Step3 from './Steps/Step3.vue'
export default {
    name: 'Stepper',
    components:{
        Step1,
        Step2,
        Step3
    },
    data:function(){
        return{
            Person: {
                FirstName:"",
                LastName:""
            },
            //visStep1: true,
            //visStep2: false,
            //visStep3: false,
            numStep: 1
        }
    },
    methods:{
        AcceptName: function(FirstName, LastName){
            this.Person.FirstName = FirstName
            this.Person.LastName = LastName

           // this.visStep1 = !this.visStep1
            //this.visStep2 = !this.visStep2

            this.numStep = this.numStep+1
        },
        next: function(){
            this.numStep = this.numStep+1
        },
        
    }
}
</script>

<style scoped>
.card{
    margin: 5% 10%;
    padding: 5% ;
}
#fon{
    background-color: blueviolet;
}
</style>