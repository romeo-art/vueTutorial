<template>
<center>
    <div id="posting">
    <center>
    <div id="divFrom" >
      <input id="inpost" v-model="mypost" class="form-control" name="mypost" placeholder="Write something here!"/><br>
    </div>
    <button id="btnSubmit" type="submit" class="btn btn-primary" @click="postnow">POST</button>
    </center>
    
    </div>
    <h2>POSTS</h2>
    <div id="mgaPosts">

    </div>

</center>

</template>
<style scoped>
    button{
        float: right;
    }
    #inpost{
        width: 600px;
        height: 200px;
    }
    #posting{
        width: 300px;
        
    }
    #mgaPosts{
        background-color: white;
        width: 100px;
        height: 50px;
    }
</style>

<script>
import AUTH from "services/auth";
import jquery from "jquery"
export default {
    data() {
        return {
            mypost: ""
        }
    },
    methods: {
        postnow: function(e){
            e.preventDefault();
            alert("WAKWAK")
        }
    }
  
}
</script>