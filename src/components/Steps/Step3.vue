<template>
    <div>
        <h1>Благодарность</h1>
        <p>Спасибо, что посетили наш сайт, {{Person.FirstName}} {{Person.LastName}}!</p>
                <v-img
                     :aspect-ratio="16/9"
                     :width="width"
                    src="https://i.gifer.com/2iFb.gif"
                 ></v-img>
    </div>
</template>

<script>
export default {
    name: 'Step3',
    props:['Person'],
    data(){
        return{
            rate: null
        }
    }
}
</script>

