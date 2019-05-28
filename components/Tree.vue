<template>
    <div>
        <div @click = "expanded = !expanded"  class = "node">
            <p align = "center">{{node.name}}</p>
         </div>
         <Tree style="padding-left:100px" v-if = "expanded" v-for="(child,index) in node.children" :key = "index"
                :node ="child"
                :depth = "depth+1"/>
    </div>
</template>
<script>
export default {
    name: 'Tree',
    props: {
        node: Object,
        depth: {
            type: Number,
            default:0
        }
    },
    data(){
        return {
            expanded: false,
        }
        
    
    }
}
</script>
<style>
.pad{
    padding-left: 40px;
}
</style>
