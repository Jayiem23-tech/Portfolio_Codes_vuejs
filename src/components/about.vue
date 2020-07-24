<template>
    <div class="about" id="about"> 
       <div class="container">
           <h1> I have <span>1 YEAR</span></h1>
           <h1>Experience in the Professional Software Development Industry</h1> 
       </div> 
    </div>
</template> 
<script>
export default {  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    *{
        list-style: none;
        text-decoration: none;
        margin:0px;
        padding:0px;
        color:black;
    } 
/* FOR WEB BROWSER */
@media(min-width:901px){
    .container{
        margin:50px; 
    }
    span{
        color:#23A155
    }
}
    /* FOR MOBILE AND TABLET */
@media (max-width:900px) {
    .container{
        margin:25px 25px; 
    }
    span{
        color:#23A155
    }
    h1{
        font-size: 1.5em;
    }
}
   
     
</style>
