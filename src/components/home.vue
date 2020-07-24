<template > 
    <div class="home" id="particles-js home"> 
         
        <div class="wrapper">
            <div class="about_container">  
                <div class="about"> 
                    <div class="headers_">  
                        <h2>Software Developer</h2>
                        <h1>Web and Desktop</h1>  
                    </div> 
                    <div class="headers_">
                        <div class="socialMediaAccout">
                            <ul>
                                <li><a href="https://github.com/Jayiem23-tech" target="_blank"><i class="fa fa-github" style="font-size:36px"/></a></li>
                                <li><a href="https://www.linkedin.com/in/john-mark-romero-a27388167" target="_blank"  ><i class="fa fa-linkedin" style="font-size:36px"/></a></li>
                            </ul>
                        </div>
                        <p class="email">Email : johnmark.romero23@gmail.com<br>
                            Contact : 09750967249</p>
                        <p class="email"></p>

                        <!-- <a href="#home" class="button">Projects</a> -->
                    </div>  
                     
                </div>
            </div> 
            <div class="mypic">  
                <img src="../assets/jm.jpg"> 
            </div> 
          
        </div>        
    </div>
    
</template>

<script>
export default {
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*{
        list-style: none;
        text-decoration: none;
        margin:0px;
        padding:0px;
        color:rgb(204, 213, 219);
    } 
      .headers_ h2 , .headers_ h1{
        color:rgb(255, 255, 255);
    } 
/* FOR MOBILE AND TABLET */ 
@media (max-width:900px) {
    .wrapper{   
         background-color: rgb(27, 38, 44); 
         position:static; 
    }
    .mypic{
        width:80%;
        margin:0 auto; 
          
    }
    img{
        width:100%;
        margin:0 auto;
    }
    .home{  
        width:100%; 
    }
    .button{ 
        
        background-color:rgb(35, 161, 85);
        color: rgb(255, 255, 255);
        border-radius: 5px;
        border-width: 1.5px;
        border-style: solid;
        border-color: rgb(35, 161, 85); 
        height: 40px;
        width:100px;
        text-align:center;
         
    }
    .about_container{
        display:flex;
        align-items:center; 
        justify-content: space-evenly; 
        width:100%; 
        margin:0px auto;
    }
    
    .about{ 
        line-height: 2em;
        color:#696969;
        font-size: 1.5em;
          
    }
    
    .email{
        font-size: .8em;
       
    }
    .headers_{
         font-size: .9em;
         margin:20% auto;
         display:flex;
         justify-content:center;
         flex-direction:column;
         align-items:center;
         height: 200px;
    }
   .headers_ h2 , .headers_ h1{
        color:white;
    }
    .headers_ h1{
        /* font-size:2em; */
    }
    .socialMediaAccout ul{ 
        display:flex;
        justify-content: center;
        align-items:center; 
        width:100px;
    }
    .socialMediaAccout ul li{
         width:100%;
         /* margin:0 100px 100px 100px; */
       /* height:100%;   */
    }
    
}
/* FOR MOBILE AND TABLET */ 
@media (max-width:944px) {
    .headers_ h1{
        font-size:2.5em;
    }
}
@media (max-width:453px) {
    .headers_ h1{
        font-size:1.7em;
    }
}
  

@media(min-width:901px){
    /* FOR WEB BROWSER */
    img{
        width:500px;
        margin:20px;
    }
    .home{
        display:flex;
        justify-content: space-evenly; 
        /* background-color:#696969; */
        background-color: rgb(27, 38, 44);
        height: 620px;
    }
    .wrapper{   
        display:flex;
        justify-content: space-evenly;
        width:100%;
    }
    .about_container{
        display:flex;
        align-items:center;  
    }
    
    .about{
         
        line-height: 4em;
        color:#696969;
    }
    .button{
        position:absolute;
        z-index: 1;
       font-size: 1.2rem;
        background-color:rgb(35, 161, 85);
        color: rgb(255, 255, 255);
        border-radius: 3px; 
        border-width: 1.5px;
        border-style: solid;
        border-color: rgb(35, 161, 85);
        border-image: initial;
        padding: 0.5rem 1rem;
        cursor:pointer; 
    }
    h1{
        font-size: 3em;
    }
    .icon{
         width:50px;
    }
     .socialMediaAccout ul{
        display:flex;
        justify-content: center;
        align-items:center; 
        width:100px;
    }
    .socialMediaAccout ul li{
         width:100%;
       /* height:100%;   */
    }
     .email{
         line-height: 1.5em;
    }
}
    
</style>
