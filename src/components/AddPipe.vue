<template>
    <q-page>
        <button @>
            ADD A PIPE
        </button>
            
       
        

    </q-page>
</template>
<script>


export default {
    data() { 
        return{
            titulo: 'titulo',
            dados: leads,
            dadosType: type,
        }
    },
    methods: {
        createPipe(data){
            
        }
    }
}
</script>

<style>
    .pipe{
    border: 2px solid grey; 
    
    display: grid;
    justify-content: center;
    align-items: center;
    }
</style>