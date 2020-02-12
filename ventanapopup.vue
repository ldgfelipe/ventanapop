<template>
<div class="gralventanapop">
<div class="backpopup" @click="cierra()" :style="'background-color:'+bgcolor+'; opacity:'+opacity+';'"></div>
<div class="infopop">
    <div class="btn btn-danger btnclose"  @click="cierra()" >
        x
    </div>
    <div class="areadatos">
        <slot></slot>
    </div>

</div>
</div>

</template>
<style>
.gralventanapop{
    position:fixed;
    top:0px;
    left:0px;
    max-width: 100%;
    max-height:100%;
    width: 100%;
    height:100%;
    z-index:9999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999;

}

.backpopup{
    background-color:#000;
    position:absolute;
    top:0px;
    left:0px;
    width:100%;
    max-width:100%;
    max-height:100%;
    height:100%;
    z-index:0;
}

.infopop{
    position:relative;
    margin:5% auto;
    width:100%;
    max-width:80%;
    height:100%;
    max-height:80%;
    background-color: #fff;
    z-index:999;
    border-radius:10px;
}

.btnclose{
    position:absolute;
    right:5px;
    top:5px;
}

.areadatos{
    width:100%;
    height:100%;
    max-height:100%;
    max-width:100%;
    overflow: auto;
    padding:10px;
    
}
</style>
<script>
module.exports={
    data(){
        return {
            
        }
    },
    methods:{
        cierra(){
            this.$emit("cerrarpop",false)
        }
    },
    props:{
        bgcolor:{
            default:'#000'
        },
        opacity:{
            default:'0.7'
        }
    }
}
</script>
