<template>
    <div class="project" id="project">
        <div class="container" v-for="project in projects" v-bind:key = "project.project_id">  
                <div class="project_header" >
                    <h2>{{project.project_id}} of 2 projects</h2>
                    <div class="pager">
                        <button  v-on:click="prev" style="font-size:15px;padding:10px;">Preview</button>
                         <button  v-on:click="next" style="font-size:15px;padding:10px 20px;">Next</button> 
                    </div> 
                </div>   
                <div class="container_company">
                    <div class="company">
                        <img :src="project.image_path" class="companyLogo">
                    </div> 
                    <div class="proj_title">
                        <h1 class="logoSpace">{{project.title}}</h1>
                        <h2 class="logoSpace">Role: {{project.role}}</h2>
                        <h3 class="logoSpace">{{project.develop_in}}</h3> 
                    </div> 
                </div>
                <div class="techlogo" >
                    <div class="techstack" v-for="(item, key, index) in project.techlogo" v-bind:key = "index">
                        <img :src="item.image_path" :alt="item.techName">
                        <p>{{item.techName}}</p>
                    </div>
                </div> 
                <div class="project_desc">
                    <p>{{project.system_desc}} </p> 
                </div>
                <div class="involvement">
                    <h3>Involvement: {{project.involvement}}</h3> 
                    <h3>Date: {{project.date}}</h3> 
                </div>  
        </div>   
    </div>
</template>

<script>
export default {
  data(){
      return { 
            projects :[{
                    project_id : '',
                    title : "",
                    role : "",
                    develop_in : "",
                    system_desc : "",
                    involvement : "",
                    date : "",
                    img:"",
                    techlogo:[]
            }],
            index:1,
            isShow:false,
      } 
  },
    methods:{ 
        pages:function(){ 
            if (this.index === 1) {
                    this.projects  = [{
                    project_id : 1,
                    title : "Accounting Management System",
                    role : "Windows Application Developer",
                    develop_in : "Developed at Omniray Ventures Inc.",
                    system_desc : "Responsibility : I maintain and create new functions/modules in the Current System and also Supporting Clients Concerns",
                    involvement : "Maintenance/Support",
                    date :"while still at Omniray Ventures Inc.",
                    img:"../assets/jm.jpg",
                    image_path : require("../assets/omniray.png"),
                    techlogo:[{
                            image_path:require("../assets/windowsLogo.png"),
                            techName:'Windows'   
                        }, {
                            image_path:require("../assets/vb.png"),
                            techName:'vb.net'   
                        }, {
                            image_path:require("../assets/database.png"),
                            techName:'Mysql'   
                    }]
                }];  
            } else if (this.index === 2){
                this.projects = [{
                    project_id : 2,
                    title : "Fixed Asset Management System",
                    role : "Windows Application Developer",
                    develop_in : "Developed at Omniray Ventures Inc.",
                    system_desc : "Responsibility : I'm responsible to Gather Informations and create the Database Logic , System Design and Functionalities for the System",
                    involvement : "Start to Finished",
                    date : "while still at Omniray Ventures Inc.",
                    image_path : require("../assets/omniray.png"),
                    techlogo:[{
                        image_path:require("../assets/windowsLogo.png"),
                        techName:'Windows'   
                    }, {
                        image_path:require("../assets/vb.png"),
                        techName:'C#'   
                    }, {
                        image_path:require("../assets/database.png"),
                        techName:' Mysql'   
                    }]
                }];  
            }  
        },
        next:function(){
            
            if (this.index <= 1) { 
                this.index++;
                this.pages();
            }
            
        },
        prev:function(){
            if (this.index >= 1) {
                this.index--;
                this.pages(); 
            }
        } 
    }, 
    created(){
         this.pages();
    },
    computed:{
        res:function(){
            this.index;
            return this.pages();
        }
    }
}
// ,{
//                    
//                 },
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*{
        list-style: none;
        text-decoration: none;
        margin:0px;
        padding:0px; 
        font-family: Verdana,Geneva,Tahoma,sans-serif;
 
    } 

/* FOR DESKTOP */
@media (min-width:901px) {
        
    .project{
        font-size:1.6em;
    }
    .container{
        /* background-color:rgb(204, 213, 219);; */
        
        height: 500px;
        margin:56px 80px;
        padding:50px 80px;
        display:flex;
        flex-direction: column;
        justify-content: space-between;
    }
    .project_header{
        display:flex;
        justify-content: space-between;
    }
    .project_header h2{
        color: #696969;
        font-size:.8em;
    }
    .container_company{
        display:flex;
        align-items: center; 
    }
    .project_desc{
        font-size: .8em;
    }
    .proj_title h1{
        font-size: 120%;
        margin-bottom:10px;
    }
     .proj_title h2{
        font-size: 100%; 
        color: rgba(17, 17, 17, 0.745);margin-bottom:10px; 
    }
    .proj_title h3{
        font-size: 75%; 
        color: rgba(53, 52, 52, 0.745);
    }
    .logoSpace{
        margin:0 15px;
       
    }
    .companyLogo{
        width:120px;
        border-radius: 80px;
        border:2px solid #696969;
    }
    .techlogo{
        display:flex;
        flex-direction:row; 
        width:100px;
    }
    .techstack{
        display:flex;
        flex-direction: row;
        align-items:center; 
        margin-left:30px;

    }
    .techstack img{
        width:60px;
    }
    .techstack p{
        font-size: .8em;
    }
    .involvement{
         font-size: .8em;
    }
}
/* FOR MOBILE AND TABLET */
@media (max-width:993px) {
    .project{
       
        font-size:.9em;
    }
    .container{ 
        height: 500px; 
        padding:50px 20px;
        display:flex;
        flex-direction: column;
        justify-content: space-between;
    }
    .project_header{
        display:flex;
        justify-content: space-between;
    }
    .project_header h2{
        color: #696969;
    }
    .container_company{
        display:flex;
        align-items: center; 
    }
    .proj_title h1{
        font-size: 150%;
        margin-bottom:10px;
    }
     .proj_title h2{
        font-size: 125%; 
        color: rgba(17, 17, 17, 0.745);margin-bottom:10px; 
    }
    .proj_title h3{
        font-size: 90%; 
        color: rgba(53, 52, 52, 0.745);
    }
    
    .logoSpace{
        margin:0 15px;
    }
    .companyLogo{
        width:120px;
        border-radius: 80px;
        border:2px solid #696969;
    }
    .techlogo{
        display:flex;
    }
    .techstack{
        display:flex;
        flex-direction: column;
        align-items:center; 
    }
    .techstack img{
        width:60px;
    }
}
    
</style>
