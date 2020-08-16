<template>
    <div class="skill_container" id="skills"> 
      <div class="skills_section">
        <h1>Tech Stack</h1>
      </div>
        <div class="container"> 
          <div class="skills">
            <div class="level">
              <p id="level_">Advanced</p>
            </div>
            <div class="wrapper">
                <div class="techlogo styling logoStyle" >
                   <img src="../assets/windowsLogo.png" alt="">
                   <h3>Windows</h3>
                </div>
                <div class="skillset styling">
                  <div class="title">VisualBasic.net / C#</div>
                  <div class="content">
                    <p>IDE: Visual Studio</p> 
                    <p>Framework: DevExpress</p>
                    <p>Database: Mysql</p> 
                  </div> 
                </div> 
            </div> 
          </div>
          <div class="skills">
            <div class="level">
              <p id="level_">Beginner</p>
            </div>
            <div class="wrapper">
                <div class="techlogo styling logoStyle" >
                   <img src="../assets/global.png" alt="">
                   <h3>Web</h3>
                </div>
                <div class="skillset styling">
                  <div class="title">Html5, Css3, js(es6), Vuejs</div>
                  <div class="content">
                    <p>Code Editor: Visual Studio Code</p> 
                    <p>Tools/Libraries: npm,particles.js</p>
                    <p>Others: Static Site Deployment to GitHub Pages / heroku</p> 
                  </div> 
                </div> 
            </div> 
          </div>
          <div class="skills">
            <div class="level">
              <p id="level_">Intermediate</p>
            </div>
            <div class="wrapper">
                <div class="techlogo styling logoStyle" >
                  <img src="../assets/database.png" alt="">
                  <h3>Backend</h3>
                </div>
                <div class="skillset styling">
                  <div class="title">Laravel</div>
                  <div class="content">
                    <p>Code Editor: Visual Studio</p> 
                    <p>Tools/Libraries: Laravel JWT</p>
                    <p>Architecture - MVC</p>
                    <p>Database: Mysql,PostgreSql</p> 
                  </div> 
                </div> 
            </div> 
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
/* FOR MOBILE AND TABLET */
@media (max-width:900px) {
  .skills_section{
      display:flex;
      justify-content: center;
      align-items: center;
      height: 80px;
    }
    .skill_container{ 
        /* background-color:#696969; */
        background-color: rgb(27, 38, 44);
        /* height: 920px;  */
    }
    .container{
        /* background-color:rgb(204, 213, 219);; */ 
        /* height: 500px; */
        /* margin:56px 80px; */
        padding:25px 10px;
        display:flex;
        flex-direction: column;
        justify-content: space-evenly;
    }
     .skills{
      width: 100%;
      /* height: 30%; */
      /* min-height: 10em; */
      padding-top: 1em;
      padding-bottom: 1em;
      display: flex;
      flex-direction: row;
      position: relative;
      border-style: solid;
      border-color: rgb(144, 183, 204);
      border-width: 1px;
      /* margin-top:10px; */
    }  
    .level{ 
        /* width: 8em;
        height: 1.5em; */
        background-color: rgb(144, 183, 204);
        position: absolute;
        right: 0px;
        top: 0px;
        display: flex;
        -webkit-box-pack: center;
        justify-content: center;
        -webkit-box-align: center;
        align-items: center;  
    }
    #level_{
      color:black;
    }
    
    .wrapper{
      display:flex;
    }
   
    .title{
      font-size: 1.3em;
    }
    .content{
      /* font-size: 1.3em; */
      line-height: 2em;
      font-style: normal; 
    }
    .techlogo{
      width:8em; 
      display:flex;
      justify-content: center;
    }
    .techlogo img{
       width:25%;
       height:30%; 
    }  
     .logoStyle{
        display:flex;
        flex-direction: column;
        align-items:center;
        font-size:.9;
    }
}
 /* FOR WEB BROWSER */
@media(min-width:901px){
  .skills_section{
      display:flex;
      justify-content: center;
      align-items: center;
      height: 80px;
    }
    .skill_container{ 
        /* background-color:#696969; */
        background-color: rgb(27, 38, 44);
        height: 920px;
      

    }
    .container{
        /* background-color:rgb(204, 213, 219);; */ 
        /* height: 500px; */
        /* margin:56px 80px; */
        padding:50px 80px;
        display:flex;
        flex-direction: column;
        justify-content: space-evenly;
    }
    .skills{
      width: 100%;
      height: 30%;
      min-height: 10em;
      padding-top: 2em;
      padding-bottom: 2em;
      display: flex;
      flex-direction: row;
      position: relative;
      border-style: solid;
      border-color: rgb(144, 183, 204);
      border-width: 1px;
      margin-top:10px;
    }
    .level{ 
        width: 8em;
        height: 1.5em;
        background-color: rgb(144, 183, 204);
        position: absolute;
        right: 0px;
        top: 0px;
        display: flex;
        -webkit-box-pack: center;
        justify-content: center;
        -webkit-box-align: center;
        align-items: center;  
    }
    #level_{
      color:black;
    }
    .wrapper{
      display:flex;
    }
   
    .title{
      font-size: 2em;
    }
    .content{
      font-size: 1.3em;
      line-height: 2em;
      font-style: normal; 
    }
    .techlogo{
      width:20em; 
      display:flex;
      justify-content: center;
    }
    .techlogo img{
       width:30%;
       height:60%; 
    }
    .logoStyle{
        display:flex;
        flex-direction: column;
        align-items:center;
    }
}

   
     
</style>
