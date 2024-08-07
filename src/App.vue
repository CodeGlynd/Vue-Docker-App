<template>
<div class="container">
<Header title="Vue App" action="Get Started" color="lightblue" bgColor="darkblue"/>


</div>
 
<div class="container">
<Header title="ToDo List" action="Add Task"/>

</div>

</template>

<script>
export default {
    name: 'App',   
    components:{
        Header
    }
    }

import Header from './Header.vue';


</script>

<style>
    
#app{
    text-align:center;
    margin-top:60px;
}

.container{
    border: 1px solid steelblue;
    padding: 30px;
    max-width: 500px;
    margin:20px auto;
}


</style> 