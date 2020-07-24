<template>
    <div class="navbar">
        <h2>
            <a href="" class="logo">John Mark</a>
        </h2>
        <input type="checkbox" name="check" id="checks" v-model="isChecked" >
        <label for="checks" class="burger_navbar">
            <i class="material-icons" style="font-size:48px;color: rgb(144, 183, 204)">menu</i>
        </label>  
        <ul> 
            <li><a href="#home" v-on:click = "checked">Home</a></li>
            <li><a href="#project" v-on:click = "checked">Projects</a></li>
            <li><a href="#skills" v-on:click = "checked">Skills</a></li>
            <li><a href="#about" v-on:click = "checked">About</a></li> 
            <li><label for="checks" class="burger_navbar">
                <i class="close-icons" style="font-size:48px;color:white">X</i>
            </label> </li>
        </ul> 
    </div>
</template> 
<script>
export default {
  name: 'HelloWorld', 
  props: {
    msg: String
  },
   data() {
       return {
           isChecked: false
       }  
  },
  methods: {
      checked:function(){
          this.isChecked = false;
      }
  }
}
</script> 
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*{
    list-style: none;
    text-decoration: none;
    margin:0px;
    padding:0px; 
}
a{
   color:white;
} 
#checks{
    display:none;
}
.logo{
    font-family:Verdana, Geneva, Tahoma, sans-serif; 
}

/* FOR MOBILE AND TABLET */
@media (max-width:900px) {
    .logo{
         font-size: 1em;
    }
    .burger_navbar{
        display:block;
    }
    .navbar{
        width:100%;
        height: 80px;
        background-color: rgb(27, 38, 44);
        display:flex;
        justify-content: space-around; 
        align-items: center;
        position: absolute;
        z-index: 2;
    } 
    ul{
        position: fixed; 
        background-color:rgb(27, 38, 44); 
        height:0;
        top:0;
        width:0; 
        display:flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        font-size: 1.7em;
        
        /* transition: width 1s ease-in-out; */
    } 
    ul li{
        display:none;
    } 
     ul li:hover , .close-icons:hover{
         background:rgb(35, 161, 85);
         cursor:pointer;
    }
    input[type="checkbox"]:checked ~ ul li{   
        width:100%; 
        text-align:center; 
        transition: height 20s ease-in-out;
        display:block;
    }
      input[type="checkbox"]:checked ~ ul{   
        top:0px;
        height: 80%;
        width:100%;
        transition: height 1s ease-in-out;
        display:flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        font-size: 1.7em;  
        /* position: absolute; */
    } 
    input[type="checkbox"] ~ ul{   
        top:0px;
        height: 0%;
        width:100%;
        transition: height 1s ease-in-out;
        display:flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        font-size: 1.7em;  
    } 
}
 /* FOR WEB BROWSER */
@media(min-width:901px){
   
    .logo{
         font-size: 1.5em;
    }
    .burger_navbar{
            display:none;
        }
    .navbar{
        width:100%;
        height: 50px;
        background-color: rgb(27, 38, 44);
        display:flex;
        justify-content: space-evenly; 
        align-items: center; 
    }  
    ul{
        display:flex;
        justify-content: space-evenly;
        width:50%;
        font-size: 18px;
    } 
    ul li{
         width:50%;
         text-align: center;
    }
     ul li:hover{
        outline:2px solid green; 
        cursor:pointer;
     } 
} 
</style>
